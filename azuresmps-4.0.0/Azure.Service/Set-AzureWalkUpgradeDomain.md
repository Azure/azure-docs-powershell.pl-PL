---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 3F3BC5AF-8D7B-40BF-A072-A11C7BDCB6B3
online version: ''
schema: 2.0.0
ms.openlocfilehash: 09adc7e9b2faf9b9a905fa1c94fb6526e02c110f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054752"
---
# <span data-ttu-id="694c8-101">Set-AzureWalkUpgradeDomain</span><span class="sxs-lookup"><span data-stu-id="694c8-101">Set-AzureWalkUpgradeDomain</span></span>

## <span data-ttu-id="694c8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="694c8-102">SYNOPSIS</span></span>
<span data-ttu-id="694c8-103">Przeprowadzi określoną domenę uaktualnienia.</span><span class="sxs-lookup"><span data-stu-id="694c8-103">Walks the specified upgrade domain.</span></span>

## <span data-ttu-id="694c8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="694c8-104">SYNTAX</span></span>

```
Set-AzureWalkUpgradeDomain [-ServiceName] <String> [-Slot] <String> [-DomainNumber] <Int32>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="694c8-105">Opis</span><span class="sxs-lookup"><span data-stu-id="694c8-105">DESCRIPTION</span></span>
<span data-ttu-id="694c8-106">Polecenie cmdlet **Set-AzureWalkUpgradeDomain** inicjuje rzeczywistą aktualizację wdrożenia platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="694c8-106">The **Set-AzureWalkUpgradeDomain** cmdlet initiates the actual upgrade of an Azure deployment.</span></span>
<span data-ttu-id="694c8-107">Pakiet i konfiguracja uaktualnienia są ustawiane przy użyciu polecenia cmdlet **Set-AzureDeployment** z przełącznikiem-Upgrade.</span><span class="sxs-lookup"><span data-stu-id="694c8-107">The upgrade package and configuration are set by using the **Set-AzureDeployment** cmdlet with the -Upgrade switch.</span></span>

## <span data-ttu-id="694c8-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="694c8-108">EXAMPLES</span></span>

### <span data-ttu-id="694c8-109">Przykład 1. inicjowanie uaktualnienia wdrożenia produkcyjnego</span><span class="sxs-lookup"><span data-stu-id="694c8-109">Example 1: Initiate an upgrade of a production deployment</span></span>
```
PS C:\> Set-AzureWalkUpgradeDomain -ServiceName "MySvc1" -slot "Production" -UpgradeDomain 2
```

<span data-ttu-id="694c8-110">To polecenie inicjuje uaktualnienie domeny uaktualnienia 2 wdrożenia produkcyjnego usługi MySvc1.</span><span class="sxs-lookup"><span data-stu-id="694c8-110">This command initiates the upgrade of Upgrade Domain 2 of the production deployment of the MySvc1 service.</span></span>

## <span data-ttu-id="694c8-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="694c8-111">PARAMETERS</span></span>

### <span data-ttu-id="694c8-112">-DomainNumber</span><span class="sxs-lookup"><span data-stu-id="694c8-112">-DomainNumber</span></span>
<span data-ttu-id="694c8-113">Określa domenę uaktualnienia do uaktualnienia.</span><span class="sxs-lookup"><span data-stu-id="694c8-113">Specifies the upgrade domain to upgrade.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="694c8-114">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="694c8-114">-InformationAction</span></span>
<span data-ttu-id="694c8-115">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="694c8-115">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="694c8-116">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="694c8-116">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="694c8-117">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="694c8-117">Continue</span></span>
- <span data-ttu-id="694c8-118">Ignorować</span><span class="sxs-lookup"><span data-stu-id="694c8-118">Ignore</span></span>
- <span data-ttu-id="694c8-119">Inquire</span><span class="sxs-lookup"><span data-stu-id="694c8-119">Inquire</span></span>
- <span data-ttu-id="694c8-120">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="694c8-120">SilentlyContinue</span></span>
- <span data-ttu-id="694c8-121">Przestaw</span><span class="sxs-lookup"><span data-stu-id="694c8-121">Stop</span></span>
- <span data-ttu-id="694c8-122">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="694c8-122">Suspend</span></span>

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

### <span data-ttu-id="694c8-123">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="694c8-123">-InformationVariable</span></span>
<span data-ttu-id="694c8-124">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="694c8-124">Specifies an information variable.</span></span>

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

### <span data-ttu-id="694c8-125">-Profile</span><span class="sxs-lookup"><span data-stu-id="694c8-125">-Profile</span></span>
<span data-ttu-id="694c8-126">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="694c8-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="694c8-127">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="694c8-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="694c8-128">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="694c8-128">-ServiceName</span></span>
<span data-ttu-id="694c8-129">Określa nazwę usługi platformy Microsoft Azure do uaktualnienia.</span><span class="sxs-lookup"><span data-stu-id="694c8-129">Specifies the Microsoft Azure service name to upgrade.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="694c8-130">-Slot</span><span class="sxs-lookup"><span data-stu-id="694c8-130">-Slot</span></span>
<span data-ttu-id="694c8-131">Określa środowisko wdrożenia do uaktualnienia.</span><span class="sxs-lookup"><span data-stu-id="694c8-131">Specifies the environment of the deployment to upgrade.</span></span>

<span data-ttu-id="694c8-132">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="694c8-132">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="694c8-133">Most</span><span class="sxs-lookup"><span data-stu-id="694c8-133">Staging</span></span>
- <span data-ttu-id="694c8-134">BOM</span><span class="sxs-lookup"><span data-stu-id="694c8-134">Production</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="694c8-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="694c8-135">CommonParameters</span></span>
<span data-ttu-id="694c8-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="694c8-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="694c8-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="694c8-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="694c8-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="694c8-138">INPUTS</span></span>

## <span data-ttu-id="694c8-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="694c8-139">OUTPUTS</span></span>

### <span data-ttu-id="694c8-140">ManagementOperationContext</span><span class="sxs-lookup"><span data-stu-id="694c8-140">ManagementOperationContext</span></span>

## <span data-ttu-id="694c8-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="694c8-141">NOTES</span></span>

## <span data-ttu-id="694c8-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="694c8-142">RELATED LINKS</span></span>

[<span data-ttu-id="694c8-143">Set-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="694c8-143">Set-AzureDeployment</span></span>](./Set-AzureDeployment.md)


