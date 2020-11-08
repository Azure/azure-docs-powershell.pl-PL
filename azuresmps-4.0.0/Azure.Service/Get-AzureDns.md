---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 184FB33A-C866-4AF0-BA31-8ADCFC6EE8E2
online version: ''
schema: 2.0.0
ms.openlocfilehash: 15ce5d8511383ad93e288b97381416d7864c3f80
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054612"
---
# <span data-ttu-id="5987c-101">Get-AzureDns</span><span class="sxs-lookup"><span data-stu-id="5987c-101">Get-AzureDns</span></span>

## <span data-ttu-id="5987c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5987c-102">SYNOPSIS</span></span>
<span data-ttu-id="5987c-103">Pobiera ustawienia DNS wdrożenia usługi Azure.</span><span class="sxs-lookup"><span data-stu-id="5987c-103">Gets the DNS settings for an Azure deployment.</span></span>

## <span data-ttu-id="5987c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5987c-104">SYNTAX</span></span>

```
Get-AzureDns [-DnsSettings <DnsSettings>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="5987c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="5987c-105">DESCRIPTION</span></span>
<span data-ttu-id="5987c-106">Polecenie cmdlet **Get-AzureDns** pobiera ustawienia DNS wdrożenia usługi Azure.</span><span class="sxs-lookup"><span data-stu-id="5987c-106">The **Get-AzureDns** cmdlet gets the DNS settings for an Azure deployment.</span></span>
<span data-ttu-id="5987c-107">Polecenie cmdlet zwraca przyjazną nazwę i adres IP serwera DNS w obiekcie ustawienia DNS.</span><span class="sxs-lookup"><span data-stu-id="5987c-107">The cmdlet returns the friendly name and IP address of the DNS server in a DNS settings object.</span></span>

## <span data-ttu-id="5987c-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5987c-108">EXAMPLES</span></span>

### <span data-ttu-id="5987c-109">Przykład 1: Pobieranie ustawień DNS</span><span class="sxs-lookup"><span data-stu-id="5987c-109">Example 1: Get DNS settings</span></span>
```
PS C:\> Get-AzureDeployment -ServiceName "ContosoService" -Slot "Production" | Get-AzureDNS
```

<span data-ttu-id="5987c-110">To polecenie używa polecenia cmdlet **Get-AzureDeployment** w celu uzyskania wdrożenia produkcyjnego usługi o nazwie ContosoService.</span><span class="sxs-lookup"><span data-stu-id="5987c-110">This command uses the **Get-AzureDeployment** cmdlet to get the production deployment of the service named ContosoService.</span></span>
<span data-ttu-id="5987c-111">Polecenie przekazuje ten obiekt do bieżącego polecenia cmdlet za pomocą operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="5987c-111">The command passes that object to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="5987c-112">Bieżące polecenie cmdlet pobiera ustawienia DNS.</span><span class="sxs-lookup"><span data-stu-id="5987c-112">The current cmdlet gets the DNS settings.</span></span>

## <span data-ttu-id="5987c-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5987c-113">PARAMETERS</span></span>

### <span data-ttu-id="5987c-114">-DnsSettings</span><span class="sxs-lookup"><span data-stu-id="5987c-114">-DnsSettings</span></span>
<span data-ttu-id="5987c-115">Określa obiekt **DnsSettings** .</span><span class="sxs-lookup"><span data-stu-id="5987c-115">Specifies a **DnsSettings** object.</span></span>

```yaml
Type: DnsSettings
Parameter Sets: (All)
Aliases: InputObject

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5987c-116">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="5987c-116">-InformationAction</span></span>
<span data-ttu-id="5987c-117">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="5987c-117">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="5987c-118">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="5987c-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="5987c-119">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="5987c-119">Continue</span></span>
- <span data-ttu-id="5987c-120">Ignorować</span><span class="sxs-lookup"><span data-stu-id="5987c-120">Ignore</span></span>
- <span data-ttu-id="5987c-121">Inquire</span><span class="sxs-lookup"><span data-stu-id="5987c-121">Inquire</span></span>
- <span data-ttu-id="5987c-122">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="5987c-122">SilentlyContinue</span></span>
- <span data-ttu-id="5987c-123">Przestaw</span><span class="sxs-lookup"><span data-stu-id="5987c-123">Stop</span></span>
- <span data-ttu-id="5987c-124">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="5987c-124">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5987c-125">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="5987c-125">-InformationVariable</span></span>
<span data-ttu-id="5987c-126">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="5987c-126">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5987c-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5987c-127">CommonParameters</span></span>
<span data-ttu-id="5987c-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5987c-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5987c-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5987c-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5987c-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5987c-130">INPUTS</span></span>

## <span data-ttu-id="5987c-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5987c-131">OUTPUTS</span></span>

## <span data-ttu-id="5987c-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5987c-132">NOTES</span></span>

## <span data-ttu-id="5987c-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5987c-133">RELATED LINKS</span></span>

[<span data-ttu-id="5987c-134">Dodaj-AzureDns</span><span class="sxs-lookup"><span data-stu-id="5987c-134">Add-AzureDns</span></span>](./Add-AzureDns.md)

[<span data-ttu-id="5987c-135">Get-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="5987c-135">Get-AzureDeployment</span></span>](./Get-AzureDeployment.md)

[<span data-ttu-id="5987c-136">Nowe — AzureDns</span><span class="sxs-lookup"><span data-stu-id="5987c-136">New-AzureDns</span></span>](./New-AzureDns.md)

[<span data-ttu-id="5987c-137">Remove-AzureDns</span><span class="sxs-lookup"><span data-stu-id="5987c-137">Remove-AzureDns</span></span>](./Remove-AzureDns.md)

[<span data-ttu-id="5987c-138">Set-AzureDns</span><span class="sxs-lookup"><span data-stu-id="5987c-138">Set-AzureDns</span></span>](./Set-AzureDns.md)


