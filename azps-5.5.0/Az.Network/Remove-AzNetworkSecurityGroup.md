---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 01F56553-1685-43D4-89E6-DDCDF17D1E00
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworksecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkSecurityGroup.md
ms.openlocfilehash: c5a5cbbbc46106fe6c388ee8f16117411f03fe0c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100240659"
---
# <span data-ttu-id="dbc46-101">Remove-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="dbc46-101">Remove-AzNetworkSecurityGroup</span></span>

## <span data-ttu-id="dbc46-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dbc46-102">SYNOPSIS</span></span>
<span data-ttu-id="dbc46-103">Usuwa grupę zabezpieczeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="dbc46-103">Removes a network security group.</span></span>

## <span data-ttu-id="dbc46-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="dbc46-104">SYNTAX</span></span>

```
Remove-AzNetworkSecurityGroup -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dbc46-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="dbc46-105">DESCRIPTION</span></span>
<span data-ttu-id="dbc46-106">Polecenie **cmdlet Remove-AzNetworkSecurityGroup** usuwa grupę zabezpieczeń sieci platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="dbc46-106">The **Remove-AzNetworkSecurityGroup** cmdlet removes an Azure network security group.</span></span>

## <span data-ttu-id="dbc46-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="dbc46-107">EXAMPLES</span></span>

### <span data-ttu-id="dbc46-108">Przykład 1. Usuwanie grupy zabezpieczeń sieci</span><span class="sxs-lookup"><span data-stu-id="dbc46-108">Example 1: Remove a network security group</span></span>
```
PS C:\>Remove-AzNetworkSecurityGroup -Name "NSG-FrontEnd" -ResourceGroupName "TestRG"
```

<span data-ttu-id="dbc46-109">To polecenie usuwa grupę zabezpieczeń o nazwie NSG-FrontEnd w grupie zasobów o nazwie TestRG.</span><span class="sxs-lookup"><span data-stu-id="dbc46-109">This command removes the security group named NSG-FrontEnd in the resource group named TestRG.</span></span>

## <span data-ttu-id="dbc46-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dbc46-110">PARAMETERS</span></span>

### <span data-ttu-id="dbc46-111">— AsJob</span><span class="sxs-lookup"><span data-stu-id="dbc46-111">-AsJob</span></span>
<span data-ttu-id="dbc46-112">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="dbc46-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="dbc46-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dbc46-113">-DefaultProfile</span></span>
<span data-ttu-id="dbc46-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="dbc46-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dbc46-115">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="dbc46-115">-Force</span></span>
<span data-ttu-id="dbc46-116">Wymusza uruchomienie polecenia bez pytania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="dbc46-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="dbc46-117">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="dbc46-117">-Name</span></span>
<span data-ttu-id="dbc46-118">Określa nazwę grupy zabezpieczeń sieciowych, która jest usuwana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dbc46-118">Specifies the name of the network security group that this cmdlet removes.</span></span>

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

### <span data-ttu-id="dbc46-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dbc46-119">-PassThru</span></span>
<span data-ttu-id="dbc46-120">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="dbc46-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="dbc46-121">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="dbc46-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="dbc46-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dbc46-122">-ResourceGroupName</span></span>
<span data-ttu-id="dbc46-123">Określa nazwę grupy zasobów, z których to polecenie cmdlet usuwa grupę zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="dbc46-123">Specifies the name of a resource group that this cmdlet removes a network security group from.</span></span>

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

### <span data-ttu-id="dbc46-124">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="dbc46-124">-Confirm</span></span>
<span data-ttu-id="dbc46-125">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="dbc46-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dbc46-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dbc46-126">-WhatIf</span></span>
<span data-ttu-id="dbc46-127">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dbc46-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dbc46-128">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="dbc46-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dbc46-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dbc46-129">CommonParameters</span></span>
<span data-ttu-id="dbc46-130">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dbc46-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dbc46-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dbc46-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dbc46-132">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dbc46-132">INPUTS</span></span>

### <span data-ttu-id="dbc46-133">System.String</span><span class="sxs-lookup"><span data-stu-id="dbc46-133">System.String</span></span>

## <span data-ttu-id="dbc46-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="dbc46-134">OUTPUTS</span></span>

### <span data-ttu-id="dbc46-135">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="dbc46-135">System.Boolean</span></span>

## <span data-ttu-id="dbc46-136">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="dbc46-136">NOTES</span></span>

## <span data-ttu-id="dbc46-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="dbc46-137">RELATED LINKS</span></span>

[<span data-ttu-id="dbc46-138">Get-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="dbc46-138">Get-AzNetworkSecurityGroup</span></span>](./Get-AzNetworkSecurityGroup.md)

[<span data-ttu-id="dbc46-139">New-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="dbc46-139">New-AzNetworkSecurityGroup</span></span>](./New-AzNetworkSecurityGroup.md)

[<span data-ttu-id="dbc46-140">Set-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="dbc46-140">Set-AzNetworkSecurityGroup</span></span>](./Set-AzNetworkSecurityGroup.md)


