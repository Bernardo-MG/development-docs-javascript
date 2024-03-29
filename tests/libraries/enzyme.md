# Enzyme

Allows testing React components.

```javascript
import React from 'react'
import { shallow, configure } from 'enzyme'
import Adapter from 'enzyme-adapter-react-16';

import ButtonInput from 'common/containers/ButtonInput';

import Button from '@material-ui/core/Button';
import TextField from '@material-ui/core/TextField';

configure({ adapter: new Adapter() });

function setup() {
   const props = {
      id: 'id',
      label: 'label',
      buttonLabel: 'buttonLabel',
      action: jest.fn()
   }

   const wrapper = shallow(<ButtonInput {...props} />)

   return {
      props,
      wrapper
   }
}

describe('<ButtonInput />', () => {
   it('handles button click when there is a value', () => {
      const { wrapper, props } = setup();
      const textField = wrapper.find(TextField);
      const button = wrapper.find(Button);

      textField.props().onChange({ target: { value: 'abc' } });
      button.simulate('click', {type: 'click'});
      expect(props.action.mock.calls.length).toBe(1);
   })
})
```

