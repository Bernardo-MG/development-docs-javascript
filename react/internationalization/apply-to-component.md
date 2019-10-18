# Apply to Component

## Using HoC

```jsx
import { injectIntl } from 'react-intl';
import messages 'i18n/messages';

function InternationalizedComponent({ intl }) {
   return <div>intl.formatMessage(messages.text)}</div>;
}

InternationalizedComponent.propTypes = {
   intl: PropTypes.object.isRequired
};

export default injectIntl(InternationalizedComponent);
```

## Using Hook

```javascript
import { useIntl} from 'react-intl';
import messages 'i18n/messages';

function InternationalizedComponent() {

   const intl = useIntl();

   return <div>intl.formatMessage(messages.text)}</div>;
}

InternationalizedComponent.propTypes = {};

export default InternationalizedComponent;
```

