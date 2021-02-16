---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvpnserverconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnServerConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnServerConfiguration.md
ms.openlocfilehash: 5d4fa487210b732e0121a01f7cc5fa392ebfb68c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100179395"
---
# <span data-ttu-id="62b89-101">Remove-AzVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="62b89-101">Remove-AzVpnServerConfiguration</span></span>

## <span data-ttu-id="62b89-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="62b89-102">SYNOPSIS</span></span>
<span data-ttu-id="62b89-103">Usuwa istniejącą konfigurację VpnServerConfiguration.</span><span class="sxs-lookup"><span data-stu-id="62b89-103">Removes an existing VpnServerConfiguration.</span></span>

## <span data-ttu-id="62b89-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="62b89-104">SYNTAX</span></span>

### <span data-ttu-id="62b89-105">ByVpnServerConfigurationName (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="62b89-105">ByVpnServerConfigurationName (Default)</span></span>
```
Remove-AzVpnServerConfiguration -ResourceGroupName <String> -Name <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="62b89-106">ByVpnServerConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="62b89-106">ByVpnServerConfigurationObject</span></span>
```
Remove-AzVpnServerConfiguration -InputObject <PSVpnServerConfiguration> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="62b89-107">ByVpnServerConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="62b89-107">ByVpnServerConfigurationResourceId</span></span>
```
Remove-AzVpnServerConfiguration -ResourceId <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="62b89-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="62b89-108">DESCRIPTION</span></span>
<span data-ttu-id="62b89-109">{{Wypełnij opis}}</span><span class="sxs-lookup"><span data-stu-id="62b89-109">{{Fill in the Description}}</span></span>

## <span data-ttu-id="62b89-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="62b89-110">EXAMPLES</span></span>

### <span data-ttu-id="62b89-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="62b89-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzVpnServerConfiguration -Name "test1config" -ResourceGroupName "P2SCortexGATesting" -Force -PassThru
```

<span data-ttu-id="62b89-112">Powyższe polecenie spowoduje usunięcie istniejącej konfiguracji VpnServerConfiguration.</span><span class="sxs-lookup"><span data-stu-id="62b89-112">The above command will remove an existing VpnServerConfiguration.</span></span>

## <span data-ttu-id="62b89-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="62b89-113">PARAMETERS</span></span>

### <span data-ttu-id="62b89-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62b89-114">-DefaultProfile</span></span>
<span data-ttu-id="62b89-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="62b89-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="62b89-116">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="62b89-116">-Force</span></span>
<span data-ttu-id="62b89-117">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="62b89-117">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="62b89-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="62b89-118">-InputObject</span></span>
<span data-ttu-id="62b89-119">Obiekt vpnServerConfiguration do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="62b89-119">The vpnServerConfiguration object to be deleted.</span></span>

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

### <span data-ttu-id="62b89-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="62b89-120">-Name</span></span>
<span data-ttu-id="62b89-121">Nazwa vpnServerConfiguration.</span><span class="sxs-lookup"><span data-stu-id="62b89-121">The vpnServerConfiguration name.</span></span>

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

### <span data-ttu-id="62b89-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="62b89-122">-PassThru</span></span>
<span data-ttu-id="62b89-123">Zwraca obiekt reprezentujący element, na którym jest wykonywana ta operacja.</span><span class="sxs-lookup"><span data-stu-id="62b89-123">Returns an object representing the item on which this operation is being performed.</span></span>

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

### <span data-ttu-id="62b89-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62b89-124">-ResourceGroupName</span></span>
<span data-ttu-id="62b89-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="62b89-125">The resource group name.</span></span>

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

### <span data-ttu-id="62b89-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="62b89-126">-ResourceId</span></span>
<span data-ttu-id="62b89-127">Identyfikator zasobu Azure dla konfiguracji vpnServerConfiguration do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="62b89-127">The Azure resource ID for the vpnServerConfiguration to be deleted.</span></span>

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

### <span data-ttu-id="62b89-128">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="62b89-128">-Confirm</span></span>
<span data-ttu-id="62b89-129">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="62b89-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="62b89-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="62b89-130">-WhatIf</span></span>
<span data-ttu-id="62b89-131">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="62b89-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="62b89-132">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="62b89-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="62b89-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62b89-133">CommonParameters</span></span>
<span data-ttu-id="62b89-134">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62b89-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62b89-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="62b89-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62b89-136">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="62b89-136">INPUTS</span></span>

### <span data-ttu-id="62b89-137">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="62b89-137">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span></span>
<span data-ttu-id="62b89-138">System.String</span><span class="sxs-lookup"><span data-stu-id="62b89-138">System.String</span></span>

## <span data-ttu-id="62b89-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="62b89-139">OUTPUTS</span></span>

### <span data-ttu-id="62b89-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="62b89-140">System.Boolean</span></span>

## <span data-ttu-id="62b89-141">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="62b89-141">NOTES</span></span>

## <span data-ttu-id="62b89-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="62b89-142">RELATED LINKS</span></span>
