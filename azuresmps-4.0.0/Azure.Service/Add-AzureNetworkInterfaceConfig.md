---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: FE31EE5C-830F-4B5E-82DB-C881032EF05C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9c1160478da2c84f2d792ab570b05d544f4537bc
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055360"
---
# <span data-ttu-id="bd21c-101">Add-AzureNetworkInterfaceConfig</span><span class="sxs-lookup"><span data-stu-id="bd21c-101">Add-AzureNetworkInterfaceConfig</span></span>

## <span data-ttu-id="bd21c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bd21c-102">SYNOPSIS</span></span>

## <span data-ttu-id="bd21c-103">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bd21c-103">SYNTAX</span></span>

```
Add-AzureNetworkInterfaceConfig [-Name] <String> [-SubnetName] <String> [[-StaticVNetIPAddress] <String>]
 [[-NetworkSecurityGroup] <String>] [[-IPForwarding] <String>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="bd21c-104">Opis</span><span class="sxs-lookup"><span data-stu-id="bd21c-104">DESCRIPTION</span></span>

## <span data-ttu-id="bd21c-105">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bd21c-105">EXAMPLES</span></span>

### <span data-ttu-id="bd21c-106">1:1</span><span class="sxs-lookup"><span data-stu-id="bd21c-106">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="bd21c-107">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bd21c-107">PARAMETERS</span></span>

### <span data-ttu-id="bd21c-108">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="bd21c-108">-InformationAction</span></span>
<span data-ttu-id="bd21c-109">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="bd21c-109">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="bd21c-110">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="bd21c-110">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="bd21c-111">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="bd21c-111">Continue</span></span>
- <span data-ttu-id="bd21c-112">Ignorować</span><span class="sxs-lookup"><span data-stu-id="bd21c-112">Ignore</span></span>
- <span data-ttu-id="bd21c-113">Inquire</span><span class="sxs-lookup"><span data-stu-id="bd21c-113">Inquire</span></span>
- <span data-ttu-id="bd21c-114">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="bd21c-114">SilentlyContinue</span></span>
- <span data-ttu-id="bd21c-115">Przestaw</span><span class="sxs-lookup"><span data-stu-id="bd21c-115">Stop</span></span>
- <span data-ttu-id="bd21c-116">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="bd21c-116">Suspend</span></span>

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

### <span data-ttu-id="bd21c-117">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="bd21c-117">-InformationVariable</span></span>
<span data-ttu-id="bd21c-118">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="bd21c-118">Specifies an information variable.</span></span>

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

### <span data-ttu-id="bd21c-119">-IPForwarding</span><span class="sxs-lookup"><span data-stu-id="bd21c-119">-IPForwarding</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd21c-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="bd21c-120">-Name</span></span>
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

### <span data-ttu-id="bd21c-121">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="bd21c-121">-NetworkSecurityGroup</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd21c-122">-Profile</span><span class="sxs-lookup"><span data-stu-id="bd21c-122">-Profile</span></span>
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

### <span data-ttu-id="bd21c-123">-StaticVNetIPAddress</span><span class="sxs-lookup"><span data-stu-id="bd21c-123">-StaticVNetIPAddress</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd21c-124">-Subnetname</span><span class="sxs-lookup"><span data-stu-id="bd21c-124">-SubnetName</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd21c-125">-VM</span><span class="sxs-lookup"><span data-stu-id="bd21c-125">-VM</span></span>
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

### <span data-ttu-id="bd21c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd21c-126">CommonParameters</span></span>
<span data-ttu-id="bd21c-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd21c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd21c-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bd21c-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd21c-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bd21c-129">INPUTS</span></span>

## <span data-ttu-id="bd21c-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bd21c-130">OUTPUTS</span></span>

## <span data-ttu-id="bd21c-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bd21c-131">NOTES</span></span>

## <span data-ttu-id="bd21c-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bd21c-132">RELATED LINKS</span></span>

[<span data-ttu-id="bd21c-133">Get-AzureNetworkInterfaceConfig</span><span class="sxs-lookup"><span data-stu-id="bd21c-133">Get-AzureNetworkInterfaceConfig</span></span>](./Get-AzureNetworkInterfaceConfig.md)

[<span data-ttu-id="bd21c-134">Remove-AzureNetworkInterfaceConfig</span><span class="sxs-lookup"><span data-stu-id="bd21c-134">Remove-AzureNetworkInterfaceConfig</span></span>](./Remove-AzureNetworkInterfaceConfig.md)

[<span data-ttu-id="bd21c-135">Set-AzureNetworkInterfaceConfig</span><span class="sxs-lookup"><span data-stu-id="bd21c-135">Set-AzureNetworkInterfaceConfig</span></span>](./Set-AzureNetworkInterfaceConfig.md)


