---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: F8E64309-7AF6-4439-841E-922B11C072AA
online version: ''
schema: 2.0.0
ms.openlocfilehash: 15dd195b86e70ad0a95484417d8cf87b0e544920
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054722"
---
# <span data-ttu-id="2c37e-101">Set-AzureNetworkSecurityGroupConfig</span><span class="sxs-lookup"><span data-stu-id="2c37e-101">Set-AzureNetworkSecurityGroupConfig</span></span>

## <span data-ttu-id="2c37e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2c37e-102">SYNOPSIS</span></span>

## <span data-ttu-id="2c37e-103">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2c37e-103">SYNTAX</span></span>

```
Set-AzureNetworkSecurityGroupConfig [-NetworkSecurityGroupName] <String> -VM <IPersistentVM>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="2c37e-104">Opis</span><span class="sxs-lookup"><span data-stu-id="2c37e-104">DESCRIPTION</span></span>

## <span data-ttu-id="2c37e-105">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2c37e-105">EXAMPLES</span></span>

### <span data-ttu-id="2c37e-106">1:1</span><span class="sxs-lookup"><span data-stu-id="2c37e-106">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="2c37e-107">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2c37e-107">PARAMETERS</span></span>

### <span data-ttu-id="2c37e-108">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="2c37e-108">-InformationAction</span></span>
<span data-ttu-id="2c37e-109">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="2c37e-109">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="2c37e-110">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="2c37e-110">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="2c37e-111">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="2c37e-111">Continue</span></span>
- <span data-ttu-id="2c37e-112">Ignorować</span><span class="sxs-lookup"><span data-stu-id="2c37e-112">Ignore</span></span>
- <span data-ttu-id="2c37e-113">Inquire</span><span class="sxs-lookup"><span data-stu-id="2c37e-113">Inquire</span></span>
- <span data-ttu-id="2c37e-114">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="2c37e-114">SilentlyContinue</span></span>
- <span data-ttu-id="2c37e-115">Przestaw</span><span class="sxs-lookup"><span data-stu-id="2c37e-115">Stop</span></span>
- <span data-ttu-id="2c37e-116">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="2c37e-116">Suspend</span></span>

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

### <span data-ttu-id="2c37e-117">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="2c37e-117">-InformationVariable</span></span>
<span data-ttu-id="2c37e-118">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="2c37e-118">Specifies an information variable.</span></span>

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

### <span data-ttu-id="2c37e-119">-NetworkSecurityGroupName</span><span class="sxs-lookup"><span data-stu-id="2c37e-119">-NetworkSecurityGroupName</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c37e-120">-Profile</span><span class="sxs-lookup"><span data-stu-id="2c37e-120">-Profile</span></span>
```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c37e-121">-VM</span><span class="sxs-lookup"><span data-stu-id="2c37e-121">-VM</span></span>
```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2c37e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c37e-122">CommonParameters</span></span>
<span data-ttu-id="2c37e-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c37e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c37e-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2c37e-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c37e-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2c37e-125">INPUTS</span></span>

## <span data-ttu-id="2c37e-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2c37e-126">OUTPUTS</span></span>

## <span data-ttu-id="2c37e-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2c37e-127">NOTES</span></span>

## <span data-ttu-id="2c37e-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2c37e-128">RELATED LINKS</span></span>

[<span data-ttu-id="2c37e-129">Remove-AzureNetworkSecurityGroupConfig</span><span class="sxs-lookup"><span data-stu-id="2c37e-129">Remove-AzureNetworkSecurityGroupConfig</span></span>](./Remove-AzureNetworkSecurityGroupConfig.md)


