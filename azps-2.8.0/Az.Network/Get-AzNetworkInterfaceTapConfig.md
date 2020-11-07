---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkinterfacetapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkInterfaceTapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkInterfaceTapConfig.md
ms.openlocfilehash: d8e9eda6c6507974376dc35e80a30669bd940153
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93870671"
---
# <span data-ttu-id="fbc7f-101">Get-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="fbc7f-101">Get-AzNetworkInterfaceTapConfig</span></span>

## <span data-ttu-id="fbc7f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fbc7f-102">SYNOPSIS</span></span>
<span data-ttu-id="fbc7f-103">Pobiera zasób konfiguracji TAP.</span><span class="sxs-lookup"><span data-stu-id="fbc7f-103">Gets a Tap configuration resource.</span></span>

## <span data-ttu-id="fbc7f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fbc7f-104">SYNTAX</span></span>

### <span data-ttu-id="fbc7f-105">GetByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="fbc7f-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzNetworkInterfaceTapConfig -ResourceGroupName <String> -NetworkInterfaceName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fbc7f-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fbc7f-106">GetByResourceIdParameterSet</span></span>
```
Get-AzNetworkInterfaceTapConfig -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fbc7f-107">Opis</span><span class="sxs-lookup"><span data-stu-id="fbc7f-107">DESCRIPTION</span></span>
<span data-ttu-id="fbc7f-108">Polecenie cmdlet **Get-AzNetworkInterfaceTapConfig umożliwia pobranie** konfiguracji platformy Azure dla danej grupy zasobów, interfejsu sieciowego i naciśnięcie nazwy konfiguracji lub listy konfiguracji naciśnij pozycję konfiguracje w grupie zasobów i interfejsie sieciowym.</span><span class="sxs-lookup"><span data-stu-id="fbc7f-108">The **Get-AzNetworkInterfaceTapConfig** cmdlet gets an Azure Tap Configuration for a given resource group, network interface and tap configuration name or list of tap configurations in a resource group and network interface.</span></span>

## <span data-ttu-id="fbc7f-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fbc7f-109">EXAMPLES</span></span>

### <span data-ttu-id="fbc7f-110">Przykład 1. Uzyskaj wszystkie konfiguracje dla danego interfejsu sieciowego</span><span class="sxs-lookup"><span data-stu-id="fbc7f-110">Example 1: Get all tap configurations for a given network interface</span></span>
```
PS C:\> Get-AzNetworkInterfaceTapConfig -ResourceGroupName "ResourceGroup1" -NetworkInterface "sourceNicName"
```

<span data-ttu-id="fbc7f-111">To polecenie umożliwia wybranie konfiguracji dodanych dla danego interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="fbc7f-111">This command gets tap configurations added for the given network interface.</span></span>

### <span data-ttu-id="fbc7f-112">Przykład 2: uzyskiwanie danej konfiguracji TAP</span><span class="sxs-lookup"><span data-stu-id="fbc7f-112">Example 2: Get a given tap configuration</span></span>
```
PS C:\> Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -NetworkInterface "sourceNicName" -Name "tapconfigName"
```

<span data-ttu-id="fbc7f-113">To polecenie pobiera określoną konfigurację wybraną dla danego interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="fbc7f-113">This command gets specific tap configuration added for the given network interface.</span></span>

### <span data-ttu-id="fbc7f-114">Przykład 3: uzyskiwanie danej konfiguracji TAP</span><span class="sxs-lookup"><span data-stu-id="fbc7f-114">Example 3: Get a given tap configuration</span></span>
```
PS C:\> Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -NetworkInterface "sourceNicName" -Name "tapconfig*"
```

<span data-ttu-id="fbc7f-115">To polecenie pobiera konfiguracje dodane dla danego interfejsu sieciowego o nazwie rozpoczynającej się od wyrazu "tapconfig".</span><span class="sxs-lookup"><span data-stu-id="fbc7f-115">This command gets tap configurations added for the given network interface with name starting with "tapconfig".</span></span>

## <span data-ttu-id="fbc7f-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fbc7f-116">PARAMETERS</span></span>

### <span data-ttu-id="fbc7f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fbc7f-117">-DefaultProfile</span></span>
<span data-ttu-id="fbc7f-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="fbc7f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbc7f-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="fbc7f-119">-Name</span></span>
<span data-ttu-id="fbc7f-120">Nazwa konkretnej konfiguracji TAP.</span><span class="sxs-lookup"><span data-stu-id="fbc7f-120">Name of the specific tap configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="fbc7f-121">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="fbc7f-121">-NetworkInterfaceName</span></span>
<span data-ttu-id="fbc7f-122">Nazwa interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="fbc7f-122">The Network Interface name.</span></span>

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

### <span data-ttu-id="fbc7f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fbc7f-123">-ResourceGroupName</span></span>
<span data-ttu-id="fbc7f-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="fbc7f-124">The resource group name.</span></span>

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

### <span data-ttu-id="fbc7f-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fbc7f-125">-ResourceId</span></span>
<span data-ttu-id="fbc7f-126">Identyfikator zasobu TapConfiguration</span><span class="sxs-lookup"><span data-stu-id="fbc7f-126">ResourceId of the TapConfiguration resource</span></span>

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

### <span data-ttu-id="fbc7f-127">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="fbc7f-127">-Confirm</span></span>
<span data-ttu-id="fbc7f-128">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fbc7f-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fbc7f-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fbc7f-129">-WhatIf</span></span>
<span data-ttu-id="fbc7f-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fbc7f-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fbc7f-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="fbc7f-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fbc7f-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbc7f-132">CommonParameters</span></span>
<span data-ttu-id="fbc7f-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fbc7f-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbc7f-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fbc7f-134">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbc7f-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fbc7f-135">INPUTS</span></span>

### <span data-ttu-id="fbc7f-136">System. String</span><span class="sxs-lookup"><span data-stu-id="fbc7f-136">System.String</span></span>

## <span data-ttu-id="fbc7f-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fbc7f-137">OUTPUTS</span></span>

### <span data-ttu-id="fbc7f-138">Microsoft. Azure. Commands. Network. models. PSNetworkInterfaceTapConfiguration</span><span class="sxs-lookup"><span data-stu-id="fbc7f-138">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceTapConfiguration</span></span>

## <span data-ttu-id="fbc7f-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fbc7f-139">NOTES</span></span>

## <span data-ttu-id="fbc7f-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fbc7f-140">RELATED LINKS</span></span>

[<span data-ttu-id="fbc7f-141">Dodaj-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="fbc7f-141">Add-AzNetworkInterfaceTapConfig</span></span>](./Add-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="fbc7f-142">Remove-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="fbc7f-142">Remove-AzNetworkInterfaceTapConfig</span></span>](./Remove-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="fbc7f-143">Set-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="fbc7f-143">Set-AzNetworkInterfaceTapConfig</span></span>](./Set-AzNetworkInterfaceTapConfig.md)
