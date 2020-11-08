---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvpnserverconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnServerConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnServerConfiguration.md
ms.openlocfilehash: 5d4fa487210b732e0121a01f7cc5fa392ebfb68c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94052904"
---
# <span data-ttu-id="0a676-101">Remove-AzVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="0a676-101">Remove-AzVpnServerConfiguration</span></span>

## <span data-ttu-id="0a676-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0a676-102">SYNOPSIS</span></span>
<span data-ttu-id="0a676-103">Usuwa istniejące VpnServerConfiguration.</span><span class="sxs-lookup"><span data-stu-id="0a676-103">Removes an existing VpnServerConfiguration.</span></span>

## <span data-ttu-id="0a676-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0a676-104">SYNTAX</span></span>

### <span data-ttu-id="0a676-105">ByVpnServerConfigurationName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="0a676-105">ByVpnServerConfigurationName (Default)</span></span>
```
Remove-AzVpnServerConfiguration -ResourceGroupName <String> -Name <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0a676-106">ByVpnServerConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="0a676-106">ByVpnServerConfigurationObject</span></span>
```
Remove-AzVpnServerConfiguration -InputObject <PSVpnServerConfiguration> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0a676-107">ByVpnServerConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="0a676-107">ByVpnServerConfigurationResourceId</span></span>
```
Remove-AzVpnServerConfiguration -ResourceId <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0a676-108">Opis</span><span class="sxs-lookup"><span data-stu-id="0a676-108">DESCRIPTION</span></span>
<span data-ttu-id="0a676-109">{{Wpisz opis}}</span><span class="sxs-lookup"><span data-stu-id="0a676-109">{{Fill in the Description}}</span></span>

## <span data-ttu-id="0a676-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0a676-110">EXAMPLES</span></span>

### <span data-ttu-id="0a676-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="0a676-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzVpnServerConfiguration -Name "test1config" -ResourceGroupName "P2SCortexGATesting" -Force -PassThru
```

<span data-ttu-id="0a676-112">Powyższe polecenie usunie istniejące VpnServerConfiguration.</span><span class="sxs-lookup"><span data-stu-id="0a676-112">The above command will remove an existing VpnServerConfiguration.</span></span>

## <span data-ttu-id="0a676-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0a676-113">PARAMETERS</span></span>

### <span data-ttu-id="0a676-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a676-114">-DefaultProfile</span></span>
<span data-ttu-id="0a676-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0a676-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a676-116">-Force</span><span class="sxs-lookup"><span data-stu-id="0a676-116">-Force</span></span>
<span data-ttu-id="0a676-117">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="0a676-117">Do not ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a676-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="0a676-118">-InputObject</span></span>
<span data-ttu-id="0a676-119">Obiekt vpnServerConfiguration, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="0a676-119">The vpnServerConfiguration object to be deleted.</span></span>

```yaml
Type: PSVpnServerConfiguration
Parameter Sets: ByVpnServerConfigurationObject
Aliases: VpnServerConfiguration

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0a676-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="0a676-120">-Name</span></span>
<span data-ttu-id="0a676-121">Nazwa vpnServerConfiguration.</span><span class="sxs-lookup"><span data-stu-id="0a676-121">The vpnServerConfiguration name.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnServerConfigurationName
Aliases: ResourceName, VpnServerConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a676-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0a676-122">-PassThru</span></span>
<span data-ttu-id="0a676-123">Zwraca obiekt reprezentujący element, dla którego wykonywana jest ta operacja.</span><span class="sxs-lookup"><span data-stu-id="0a676-123">Returns an object representing the item on which this operation is being performed.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a676-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a676-124">-ResourceGroupName</span></span>
<span data-ttu-id="0a676-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="0a676-125">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnServerConfigurationName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a676-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0a676-126">-ResourceId</span></span>
<span data-ttu-id="0a676-127">Identyfikator zasobu platformy Azure dla vpnServerConfiguration, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="0a676-127">The Azure resource ID for the vpnServerConfiguration to be deleted.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnServerConfigurationResourceId
Aliases: VpnServerConfigurationId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a676-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0a676-128">-Confirm</span></span>
<span data-ttu-id="0a676-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0a676-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a676-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0a676-130">-WhatIf</span></span>
<span data-ttu-id="0a676-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0a676-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0a676-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="0a676-132">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a676-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a676-133">CommonParameters</span></span>
<span data-ttu-id="0a676-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0a676-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a676-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0a676-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a676-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0a676-136">INPUTS</span></span>

### <span data-ttu-id="0a676-137">Microsoft. Azure. Commands. Network. models. PSVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="0a676-137">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span></span>
<span data-ttu-id="0a676-138">System. String</span><span class="sxs-lookup"><span data-stu-id="0a676-138">System.String</span></span>

## <span data-ttu-id="0a676-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0a676-139">OUTPUTS</span></span>

### <span data-ttu-id="0a676-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0a676-140">System.Boolean</span></span>

## <span data-ttu-id="0a676-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0a676-141">NOTES</span></span>

## <span data-ttu-id="0a676-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0a676-142">RELATED LINKS</span></span>
