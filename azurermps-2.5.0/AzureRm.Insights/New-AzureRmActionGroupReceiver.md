---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 9830CD16-D797-47EB-BEF5-6CFE3454BCAA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/new-azurermactiongroupreceiver
schema: 2.0.0
ms.openlocfilehash: 0f452818db1af3f3a69db58f82b89e6cfa8ee461
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93897441"
---
# <span data-ttu-id="bc62b-101">New-AzureRmActionGroupReceiver</span><span class="sxs-lookup"><span data-stu-id="bc62b-101">New-AzureRmActionGroupReceiver</span></span>

## <span data-ttu-id="bc62b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bc62b-102">SYNOPSIS</span></span>
<span data-ttu-id="bc62b-103">Tworzy nowy odbiorcę grupy akcji.</span><span class="sxs-lookup"><span data-stu-id="bc62b-103">Creates an new action group receiver.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bc62b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bc62b-104">SYNTAX</span></span>

### <span data-ttu-id="bc62b-105">NewEmailReceiver (domyślny)</span><span class="sxs-lookup"><span data-stu-id="bc62b-105">NewEmailReceiver (Default)</span></span>
```
New-AzureRmActionGroupReceiver -Name <String> [-EmailReceiver] -EmailAddress <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bc62b-106">NewSmsReceiver</span><span class="sxs-lookup"><span data-stu-id="bc62b-106">NewSmsReceiver</span></span>
```
New-AzureRmActionGroupReceiver -Name <String> [-SmsReceiver] [-CountryCode <String>] -PhoneNumber <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bc62b-107">NewWebhookReceiver</span><span class="sxs-lookup"><span data-stu-id="bc62b-107">NewWebhookReceiver</span></span>
```
New-AzureRmActionGroupReceiver -Name <String> [-WebhookReceiver] -ServiceUri <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bc62b-108">Opis</span><span class="sxs-lookup"><span data-stu-id="bc62b-108">DESCRIPTION</span></span>
<span data-ttu-id="bc62b-109">Polecenie cmdlet **New-AzureRmActionGroupReceiver** umożliwia utworzenie nowego adresata grupy akcji w pamięci.</span><span class="sxs-lookup"><span data-stu-id="bc62b-109">The **New-AzureRmActionGroupReceiver** cmdlet creates new action group receiver in memory.</span></span>

## <span data-ttu-id="bc62b-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bc62b-110">EXAMPLES</span></span>

### <span data-ttu-id="bc62b-111">Przykład 1: Utwórz nowy odbiornik poczty E-mail w pamięci.</span><span class="sxs-lookup"><span data-stu-id="bc62b-111">Example 1: Create a new Email receiver in memory.</span></span>
```
PS C:\>$emailReceiver = New-AzureRmActionGroupReceiver -Name 'emailReceiver1' -EmailReceiver -EmailAddress 'user1@example.com'
```

<span data-ttu-id="bc62b-112">To polecenie tworzy nowy odbiornik poczty E-mail w pamięci.</span><span class="sxs-lookup"><span data-stu-id="bc62b-112">This command creates a new Email receiver in memory.</span></span>

### <span data-ttu-id="bc62b-113">Przykład 2: Utwórz nowy odbiornik SMS w pamięci.</span><span class="sxs-lookup"><span data-stu-id="bc62b-113">Example 2: Create a new SMS receiver in memory.</span></span>
```
PS C:\>$smsReceiver = New-AzureRmActionGroupReceiver -Name 'smsReceiver1' -SmsReceiver -CountryCode '1' -PhoneNumber '5555555555'
```

<span data-ttu-id="bc62b-114">To polecenie tworzy nowy odbiornik SMS w pamięci.</span><span class="sxs-lookup"><span data-stu-id="bc62b-114">This command creates a new SMS receiver in memory.</span></span>

### <span data-ttu-id="bc62b-115">Przykład 3: Tworzenie nowego odbiornika webhook w pamięci.</span><span class="sxs-lookup"><span data-stu-id="bc62b-115">Example 3: Create a new webhook receiver in memory.</span></span>
```
PS C:\>$webhookReceiver = New-AzureRmActionGroupReceiver -Name 'webhookReceiver1' -SMSReceiver -ServiceUri 'http://test.com'
```

<span data-ttu-id="bc62b-116">To polecenie tworzy nowy odbiornik elementu webhook w pamięci.</span><span class="sxs-lookup"><span data-stu-id="bc62b-116">This command creates a new webhook receiver in memory.</span></span>

## <span data-ttu-id="bc62b-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bc62b-117">PARAMETERS</span></span>

### <span data-ttu-id="bc62b-118">-CountryCode</span><span class="sxs-lookup"><span data-stu-id="bc62b-118">-CountryCode</span></span>
<span data-ttu-id="bc62b-119">Określa numer kierunkowy kraju odbiorcy wiadomości SMS.</span><span class="sxs-lookup"><span data-stu-id="bc62b-119">Specifies the country code for the SMS receiver.</span></span>

```yaml
Type: System.String
Parameter Sets: NewSmsReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc62b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc62b-120">-DefaultProfile</span></span>
<span data-ttu-id="bc62b-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="bc62b-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc62b-122">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="bc62b-122">-EmailAddress</span></span>
<span data-ttu-id="bc62b-123">Określa adres odbiorcy poczty E-mail.</span><span class="sxs-lookup"><span data-stu-id="bc62b-123">Specifies the address for the Email receiver.</span></span>

```yaml
Type: System.String
Parameter Sets: NewEmailReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc62b-124">-EmailReceiver</span><span class="sxs-lookup"><span data-stu-id="bc62b-124">-EmailReceiver</span></span>
<span data-ttu-id="bc62b-125">Określa, aby utworzyć odbiorcę poczty E-mail</span><span class="sxs-lookup"><span data-stu-id="bc62b-125">Specifies to create an Email receiver</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: NewEmailReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc62b-126">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="bc62b-126">-Name</span></span>
<span data-ttu-id="bc62b-127">Określa nazwę odbiornika.</span><span class="sxs-lookup"><span data-stu-id="bc62b-127">Specifies the name for the receiver.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc62b-128">-Rachunek</span><span class="sxs-lookup"><span data-stu-id="bc62b-128">-PhoneNumber</span></span>
<span data-ttu-id="bc62b-129">Określa numer telefonu odbiornika SMS.</span><span class="sxs-lookup"><span data-stu-id="bc62b-129">Specifies the phone number for the SMS receiver.</span></span>

```yaml
Type: System.String
Parameter Sets: NewSmsReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc62b-130">-ServiceUri</span><span class="sxs-lookup"><span data-stu-id="bc62b-130">-ServiceUri</span></span>
<span data-ttu-id="bc62b-131">Określa identyfikator URI odbiornika webhook.</span><span class="sxs-lookup"><span data-stu-id="bc62b-131">Specifies the URI for the webhook receiver.</span></span>

```yaml
Type: System.String
Parameter Sets: NewWebhookReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc62b-132">-SmsReceiver</span><span class="sxs-lookup"><span data-stu-id="bc62b-132">-SmsReceiver</span></span>
<span data-ttu-id="bc62b-133">Określa, aby utworzyć odbiorcę wiadomości SMS</span><span class="sxs-lookup"><span data-stu-id="bc62b-133">Specifies to create a SMS receiver</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: NewSmsReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc62b-134">-WebhookReceiver</span><span class="sxs-lookup"><span data-stu-id="bc62b-134">-WebhookReceiver</span></span>
<span data-ttu-id="bc62b-135">Określa, aby utworzyć odbiornik elementu webhook</span><span class="sxs-lookup"><span data-stu-id="bc62b-135">Specifies to create a webhook receiver</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: NewWebhookReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc62b-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc62b-136">CommonParameters</span></span>
<span data-ttu-id="bc62b-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bc62b-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc62b-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bc62b-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc62b-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bc62b-139">INPUTS</span></span>

### <span data-ttu-id="bc62b-140">System. String</span><span class="sxs-lookup"><span data-stu-id="bc62b-140">System.String</span></span>

### <span data-ttu-id="bc62b-141">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="bc62b-141">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="bc62b-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bc62b-142">OUTPUTS</span></span>

### <span data-ttu-id="bc62b-143">Microsoft. Azure. Commands. Insights. OutputClasses. PSActionGroupReceiverBase</span><span class="sxs-lookup"><span data-stu-id="bc62b-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase</span></span>

## <span data-ttu-id="bc62b-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bc62b-144">NOTES</span></span>

## <span data-ttu-id="bc62b-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bc62b-145">RELATED LINKS</span></span>

<span data-ttu-id="bc62b-146">[Set-AzureRmActionGroup](./Set-AzureRmActionGroup.md) 
 [Get-AzureRmActionGroup](./Get-AzureRmActionGroup.md) 
 [Remove-AzureRmActionGroup](./Remove-AzureRmActionGroup.md)</span><span class="sxs-lookup"><span data-stu-id="bc62b-146">[Set-AzureRmActionGroup](./Set-AzureRmActionGroup.md)
[Get-AzureRmActionGroup](./Get-AzureRmActionGroup.md)
[Remove-AzureRmActionGroup](./Remove-AzureRmActionGroup.md)</span></span>
