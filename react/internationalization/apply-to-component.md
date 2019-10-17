# Apply to Component

## Using HoC

```jsx
import { injectIntl } from 'react-intl';
import messages 'i18n/messages';

const InternationalizedComponent = () =>
   <div>props.intl.formatMessage(messages.text)}</div>

InternationalizedComponent .propTypes = {
   intl: intlShape.isRequired
};

export default injectIntl(InternationalizedComponent );
```

