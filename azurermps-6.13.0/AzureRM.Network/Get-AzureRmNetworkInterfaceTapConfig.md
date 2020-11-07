---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkinterfacetapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkInterfaceTapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkInterfaceTapConfig.md
ms.openlocfilehash: 2f6c4f410c7d4f92c8dcd911e0c113f2a91b304c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719563"
---
# <span data-ttu-id="c9c73-101">Get-AzureRmNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="c9c73-101">Get-AzureRmNetworkInterfaceTapConfig</span></span>

## <span data-ttu-id="c9c73-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c9c73-102">SYNOPSIS</span></span>
<span data-ttu-id="c9c73-103">Pobiera zasób konfiguracji TAP.</span><span class="sxs-lookup"><span data-stu-id="c9c73-103">Gets a Tap configuration resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c9c73-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c9c73-104">SYNTAX</span></span>

### <span data-ttu-id="c9c73-105">GetByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="c9c73-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzureRmNetworkInterfaceTapConfig -ResourceGroupName <String> -NetworkInterfaceName <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c9c73-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c9c73-106">GetByResourceIdParameterSet</span></span>
```
Get-AzureRmNetworkInterfaceTapConfig -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c9c73-107">Opis</span><span class="sxs-lookup"><span data-stu-id="c9c73-107">DESCRIPTION</span></span>
<span data-ttu-id="c9c73-108">Polecenie cmdlet **Get-AzureRmNetworkInterfaceTapConfig umożliwia pobranie** konfiguracji platformy Azure dla danej grupy zasobów, interfejsu sieciowego i naciśnięcie nazwy konfiguracji lub listy konfiguracji naciśnij pozycję konfiguracje w grupie zasobów i interfejsie sieciowym.</span><span class="sxs-lookup"><span data-stu-id="c9c73-108">The **Get-AzureRmNetworkInterfaceTapConfig** cmdlet gets an Azure Tap Configuration for a given resource group, network interface and tap configuration name or list of tap configurations in a resource group and network interface.</span></span>

## <span data-ttu-id="c9c73-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c9c73-109">EXAMPLES</span></span>

### <span data-ttu-id="c9c73-110">Przykład 1. Uzyskaj wszystkie konfiguracje dla danego interfejsu sieciowego</span><span class="sxs-lookup"><span data-stu-id="c9c73-110">Example 1: Get all tap configurations for a given network interface</span></span>
```
PS C:\>Get-AzureRmNetworkInterfaceTapConfig -ResourceGroupName "ResourceGroup1" -NetworkInterface "sourceNicName"
```

<span data-ttu-id="c9c73-111">To polecenie umożliwia wybranie konfiguracji dodanych dla danego interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="c9c73-111">This command gets tap configurations added for the given network interface.</span></span>

### <span data-ttu-id="c9c73-112">Przykład 2: uzyskiwanie danej konfiguracji TAP</span><span class="sxs-lookup"><span data-stu-id="c9c73-112">Example 2: Get a given tap configuration</span></span>
```
PS C:\>Get-AzureRmNetworkInterface -ResourceGroupName "ResourceGroup1" -NetworkInterface "sourceNicName" -Name "tapconfigName"
```

<span data-ttu-id="c9c73-113">To polecenie pobiera określoną konfigurację wybraną dla danego interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="c9c73-113">This command gets specific tap configuration added for the given network interface.</span></span>

## <span data-ttu-id="c9c73-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c9c73-114">PARAMETERS</span></span>

### <span data-ttu-id="c9c73-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9c73-115">-DefaultProfile</span></span>
<span data-ttu-id="c9c73-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c9c73-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c9c73-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c9c73-117">-Name</span></span>
<span data-ttu-id="c9c73-118">Nazwa konkretnej konfiguracji TAP.</span><span class="sxs-lookup"><span data-stu-id="c9c73-118">Name of the specific tap configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9c73-119">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="c9c73-119">-NetworkInterfaceName</span></span>
<span data-ttu-id="c9c73-120">Nazwa interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="c9c73-120">The Network Interface name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9c73-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9c73-121">-ResourceGroupName</span></span>
<span data-ttu-id="c9c73-122">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="c9c73-122">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9c73-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c9c73-123">-ResourceId</span></span>
<span data-ttu-id="c9c73-124">Identyfikator zasobu TapConfiguration</span><span class="sxs-lookup"><span data-stu-id="c9c73-124">ResourceId of the TapConfiguration resource</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9c73-125">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c9c73-125">-Confirm</span></span>
<span data-ttu-id="c9c73-126">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c9c73-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c9c73-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c9c73-127">-WhatIf</span></span>
<span data-ttu-id="c9c73-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c9c73-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c9c73-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="c9c73-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c9c73-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9c73-130">CommonParameters</span></span>
<span data-ttu-id="c9c73-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c9c73-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9c73-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c9c73-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9c73-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c9c73-133">INPUTS</span></span>

### <span data-ttu-id="c9c73-134">System. String</span><span class="sxs-lookup"><span data-stu-id="c9c73-134">System.String</span></span>

## <span data-ttu-id="c9c73-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c9c73-135">OUTPUTS</span></span>

### <span data-ttu-id="c9c73-136">Microsoft. Azure. Commands. Network. models. PSNetworkInterfaceTapConfiguration</span><span class="sxs-lookup"><span data-stu-id="c9c73-136">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceTapConfiguration</span></span>

## <span data-ttu-id="c9c73-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c9c73-137">NOTES</span></span>

## <span data-ttu-id="c9c73-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c9c73-138">RELATED LINKS</span></span>