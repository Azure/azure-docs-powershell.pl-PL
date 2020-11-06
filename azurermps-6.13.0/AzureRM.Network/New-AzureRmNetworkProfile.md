---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermnetworkprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkProfile.md
ms.openlocfilehash: fedf6818f95bd5afadb92c1423a1dbb3296727e2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93545043"
---
# <span data-ttu-id="be3d2-101">New-AzureRmNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="be3d2-101">New-AzureRmNetworkProfile</span></span>

## <span data-ttu-id="be3d2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="be3d2-102">SYNOPSIS</span></span>
<span data-ttu-id="be3d2-103">Tworzy nowy profil sieciowy.</span><span class="sxs-lookup"><span data-stu-id="be3d2-103">Creates a new network profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="be3d2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="be3d2-104">SYNTAX</span></span>

```
New-AzureRmNetworkProfile -ResourceGroupName <String> -Name <String> [-Location <String>] [-Tag <Hashtable>]
 [-ContainerNicConfig <PSContainerNetworkInterfaceConfiguration[]>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="be3d2-105">Opis</span><span class="sxs-lookup"><span data-stu-id="be3d2-105">DESCRIPTION</span></span>
<span data-ttu-id="be3d2-106">Polecenie cmdlet **New-AzureRmNetworkProfile** tworzy nowy zasób najwyższego poziomu profilu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="be3d2-106">The **New-AzureRmNetworkProfile** cmdlet creates a new network profile top level resource.</span></span>

## <span data-ttu-id="be3d2-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="be3d2-107">EXAMPLES</span></span>

### <span data-ttu-id="be3d2-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="be3d2-108">Example 1</span></span>
```powershell
$networkProfile = New-AzureRmNetworkProfile -Name np1 -ResourceGroupName rg1 -Location westus
```

<span data-ttu-id="be3d2-109">Spowoduje to utworzenie nowego zasobu najwyższego poziomu profilu sieciowego</span><span class="sxs-lookup"><span data-stu-id="be3d2-109">This creates a new network profile top level resource</span></span>

## <span data-ttu-id="be3d2-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="be3d2-110">PARAMETERS</span></span>

### <span data-ttu-id="be3d2-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="be3d2-111">-AsJob</span></span>
<span data-ttu-id="be3d2-112">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="be3d2-112">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be3d2-113">-ContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="be3d2-113">-ContainerNicConfig</span></span>
<span data-ttu-id="be3d2-114">Konfiguracja interfejsu sieciowego kontenera do dodania do tego profilu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="be3d2-114">The container network interface configurations to add to this network profile.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSContainerNetworkInterfaceConfiguration[]
Parameter Sets: (All)
Aliases: ContainerNetworkInterfaceConfiguration

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be3d2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be3d2-115">-DefaultProfile</span></span>
<span data-ttu-id="be3d2-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="be3d2-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="be3d2-117">-Force</span><span class="sxs-lookup"><span data-stu-id="be3d2-117">-Force</span></span>
<span data-ttu-id="be3d2-118">Nie pytaj o potwierdzenie zamiaru zastąpienia zasobu</span><span class="sxs-lookup"><span data-stu-id="be3d2-118">Do not ask for confirmation if you want to overwrite a resource</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be3d2-119">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="be3d2-119">-Location</span></span>
<span data-ttu-id="be3d2-120">Lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="be3d2-120">The location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be3d2-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="be3d2-121">-Name</span></span>
<span data-ttu-id="be3d2-122">Nazwa profilu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="be3d2-122">The name of the network profile.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be3d2-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="be3d2-123">-ResourceGroupName</span></span>
<span data-ttu-id="be3d2-124">Nazwa grupy zasobów profilu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="be3d2-124">The resource group name of the network profile.</span></span>

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

### <span data-ttu-id="be3d2-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="be3d2-125">-Tag</span></span>
<span data-ttu-id="be3d2-126">Obiekt Hashtable reprezentujący znaczniki zasobów.</span><span class="sxs-lookup"><span data-stu-id="be3d2-126">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be3d2-127">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="be3d2-127">-Confirm</span></span>
<span data-ttu-id="be3d2-128">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="be3d2-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be3d2-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="be3d2-129">-WhatIf</span></span>
<span data-ttu-id="be3d2-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="be3d2-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="be3d2-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="be3d2-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be3d2-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be3d2-132">CommonParameters</span></span>
<span data-ttu-id="be3d2-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="be3d2-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be3d2-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="be3d2-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be3d2-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="be3d2-135">INPUTS</span></span>

### <span data-ttu-id="be3d2-136">System. String</span><span class="sxs-lookup"><span data-stu-id="be3d2-136">System.String</span></span>

### <span data-ttu-id="be3d2-137">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="be3d2-137">System.Collections.Hashtable</span></span>

### <span data-ttu-id="be3d2-138">System. Collections. Generic. list "1 [[Microsoft. Azure. Commands. Network. MODELES. PSContainerNetworkInterface; Microsoft. Azure. Commands. Network, Version = 6.7.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="be3d2-138">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSContainerNetworkInterface, Microsoft.Azure.Commands.Network, Version=6.7.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="be3d2-139">System. Collections. Generic. list "1 [[Microsoft. Azure. Commands. Network. MODELES. PSContainerNetworkInterfaceConfiguration; Microsoft. Azure. Commands. Network, Version = 6.7.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="be3d2-139">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSContainerNetworkInterfaceConfiguration, Microsoft.Azure.Commands.Network, Version=6.7.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="be3d2-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="be3d2-140">OUTPUTS</span></span>

### <span data-ttu-id="be3d2-141">Microsoft. Azure. Commands. Network. models. PSNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="be3d2-141">Microsoft.Azure.Commands.Network.Models.PSNetworkProfile</span></span>

## <span data-ttu-id="be3d2-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="be3d2-142">NOTES</span></span>

## <span data-ttu-id="be3d2-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="be3d2-143">RELATED LINKS</span></span>
