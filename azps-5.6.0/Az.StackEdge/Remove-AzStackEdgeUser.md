---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/powershell/module/az.stackedge/remove-azstackedgeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeUser.md
ms.openlocfilehash: 5dd0da12115b41e7579c8a34e436a85f8614ed81
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102005050"
---
# <span data-ttu-id="24209-101">Remove-AzStackEdgeUser</span><span class="sxs-lookup"><span data-stu-id="24209-101">Remove-AzStackEdgeUser</span></span>

## <span data-ttu-id="24209-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="24209-102">SYNOPSIS</span></span>
<span data-ttu-id="24209-103">Usuwa użytkownika z urządzenia.</span><span class="sxs-lookup"><span data-stu-id="24209-103">Removes a user on a device.</span></span>

## <span data-ttu-id="24209-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="24209-104">SYNTAX</span></span>

### <span data-ttu-id="24209-105">DeleteByNameParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="24209-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzStackEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="24209-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="24209-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzStackEdgeUser [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="24209-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="24209-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzStackEdgeUser [-InputObject] <PSStackEdgeUser> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="24209-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="24209-108">DESCRIPTION</span></span>
<span data-ttu-id="24209-109">Polecenie **cmdlet Remove-AzStackEdgeUser** usuwa użytkownika z urządzenia Stack Edge.</span><span class="sxs-lookup"><span data-stu-id="24209-109">The **Remove-AzStackEdgeUser** cmdlet removes a user on the Stack Edge device.</span></span> <span data-ttu-id="24209-110">Obsługiwane jest tworzenie tylko użytkowników `Share` tego typu.</span><span class="sxs-lookup"><span data-stu-id="24209-110">Creation of only users of type `Share` is supported.</span></span>

## <span data-ttu-id="24209-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="24209-111">EXAMPLES</span></span>

### <span data-ttu-id="24209-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="24209-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzStackEdgeUser -ResourceGroupName resourceGroupName -DeviceName deviceName -Name username
```

## <span data-ttu-id="24209-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="24209-113">PARAMETERS</span></span>

### <span data-ttu-id="24209-114">— AsJob</span><span class="sxs-lookup"><span data-stu-id="24209-114">-AsJob</span></span>
<span data-ttu-id="24209-115">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="24209-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="24209-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24209-116">-DefaultProfile</span></span>
<span data-ttu-id="24209-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="24209-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="24209-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="24209-118">-DeviceName</span></span>
<span data-ttu-id="24209-119">Nazwa urządzenia</span><span class="sxs-lookup"><span data-stu-id="24209-119">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24209-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="24209-120">-InputObject</span></span>
<span data-ttu-id="24209-121">Obiekt Input</span><span class="sxs-lookup"><span data-stu-id="24209-121">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeUser
Parameter Sets: DeleteByInputObjectParameterSet
Aliases: User

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="24209-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="24209-122">-Name</span></span>
<span data-ttu-id="24209-123">Nazwa użytkownika</span><span class="sxs-lookup"><span data-stu-id="24209-123">Username</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases: Username

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24209-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="24209-124">-PassThru</span></span>
<span data-ttu-id="24209-125">zwraca wartość prawda, jeśli pomyślnie</span><span class="sxs-lookup"><span data-stu-id="24209-125">returns true if successful</span></span>

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

### <span data-ttu-id="24209-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24209-126">-ResourceGroupName</span></span>
<span data-ttu-id="24209-127">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="24209-127">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24209-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="24209-128">-ResourceId</span></span>
<span data-ttu-id="24209-129">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="24209-129">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24209-130">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="24209-130">-Confirm</span></span>
<span data-ttu-id="24209-131">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="24209-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="24209-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24209-132">-WhatIf</span></span>
<span data-ttu-id="24209-133">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="24209-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="24209-134">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="24209-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="24209-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24209-135">CommonParameters</span></span>
<span data-ttu-id="24209-136">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24209-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24209-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="24209-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24209-138">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="24209-138">INPUTS</span></span>

### <span data-ttu-id="24209-139">System.String</span><span class="sxs-lookup"><span data-stu-id="24209-139">System.String</span></span>

### <span data-ttu-id="24209-140">Microsoft.Azure.PowerShell.Cmdlet.StackEdge.Models.PSStackEdgeUser</span><span class="sxs-lookup"><span data-stu-id="24209-140">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeUser</span></span>

## <span data-ttu-id="24209-141">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="24209-141">OUTPUTS</span></span>

### <span data-ttu-id="24209-142">Microsoft.Azure.PowerShell.Cmdlet.StackEdge.Models.PSStackEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="24209-142">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="24209-143">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="24209-143">NOTES</span></span>

## <span data-ttu-id="24209-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="24209-144">RELATED LINKS</span></span>
