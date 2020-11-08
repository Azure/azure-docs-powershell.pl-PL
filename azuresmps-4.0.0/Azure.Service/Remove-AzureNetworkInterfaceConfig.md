---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 185C2680-501F-497D-81B2-5F6E30A91F16
online version: ''
schema: 2.0.0
ms.openlocfilehash: 55e9f6f026e7e524613a0e070767bc2ab26f6d66
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055432"
---
# <span data-ttu-id="24a4b-101">Remove-AzureNetworkInterfaceConfig</span><span class="sxs-lookup"><span data-stu-id="24a4b-101">Remove-AzureNetworkInterfaceConfig</span></span>

## <span data-ttu-id="24a4b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="24a4b-102">SYNOPSIS</span></span>

## <span data-ttu-id="24a4b-103">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="24a4b-103">SYNTAX</span></span>

```
Remove-AzureNetworkInterfaceConfig [-Name] <String> -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="24a4b-104">Opis</span><span class="sxs-lookup"><span data-stu-id="24a4b-104">DESCRIPTION</span></span>

## <span data-ttu-id="24a4b-105">Przykłady</span><span class="sxs-lookup"><span data-stu-id="24a4b-105">EXAMPLES</span></span>

### <span data-ttu-id="24a4b-106">1:1</span><span class="sxs-lookup"><span data-stu-id="24a4b-106">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="24a4b-107">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="24a4b-107">PARAMETERS</span></span>

### <span data-ttu-id="24a4b-108">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="24a4b-108">-InformationAction</span></span>
<span data-ttu-id="24a4b-109">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="24a4b-109">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="24a4b-110">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="24a4b-110">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="24a4b-111">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="24a4b-111">Continue</span></span>
- <span data-ttu-id="24a4b-112">Ignorować</span><span class="sxs-lookup"><span data-stu-id="24a4b-112">Ignore</span></span>
- <span data-ttu-id="24a4b-113">Inquire</span><span class="sxs-lookup"><span data-stu-id="24a4b-113">Inquire</span></span>
- <span data-ttu-id="24a4b-114">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="24a4b-114">SilentlyContinue</span></span>
- <span data-ttu-id="24a4b-115">Przestaw</span><span class="sxs-lookup"><span data-stu-id="24a4b-115">Stop</span></span>
- <span data-ttu-id="24a4b-116">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="24a4b-116">Suspend</span></span>

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

### <span data-ttu-id="24a4b-117">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="24a4b-117">-InformationVariable</span></span>
<span data-ttu-id="24a4b-118">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="24a4b-118">Specifies an information variable.</span></span>

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

### <span data-ttu-id="24a4b-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="24a4b-119">-Name</span></span>
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

### <span data-ttu-id="24a4b-120">-Profile</span><span class="sxs-lookup"><span data-stu-id="24a4b-120">-Profile</span></span>
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

### <span data-ttu-id="24a4b-121">-VM</span><span class="sxs-lookup"><span data-stu-id="24a4b-121">-VM</span></span>
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

### <span data-ttu-id="24a4b-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24a4b-122">CommonParameters</span></span>
<span data-ttu-id="24a4b-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24a4b-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24a4b-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24a4b-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24a4b-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="24a4b-125">INPUTS</span></span>

## <span data-ttu-id="24a4b-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="24a4b-126">OUTPUTS</span></span>

## <span data-ttu-id="24a4b-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="24a4b-127">NOTES</span></span>

## <span data-ttu-id="24a4b-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="24a4b-128">RELATED LINKS</span></span>

[<span data-ttu-id="24a4b-129">Dodaj-AzureNetworkInterfaceConfig</span><span class="sxs-lookup"><span data-stu-id="24a4b-129">Add-AzureNetworkInterfaceConfig</span></span>](./Add-AzureNetworkInterfaceConfig.md)

[<span data-ttu-id="24a4b-130">Get-AzureNetworkInterfaceConfig</span><span class="sxs-lookup"><span data-stu-id="24a4b-130">Get-AzureNetworkInterfaceConfig</span></span>](./Get-AzureNetworkInterfaceConfig.md)

[<span data-ttu-id="24a4b-131">Set-AzureNetworkInterfaceConfig</span><span class="sxs-lookup"><span data-stu-id="24a4b-131">Set-AzureNetworkInterfaceConfig</span></span>](./Set-AzureNetworkInterfaceConfig.md)


