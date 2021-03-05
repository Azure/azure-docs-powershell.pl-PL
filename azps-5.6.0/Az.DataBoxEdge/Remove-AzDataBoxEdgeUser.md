---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/powershell/module/az.databoxedge/remove-azdataboxedgeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeUser.md
ms.openlocfilehash: 8c977c61f332ccdc927dd3f0e070d635e6095acf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101983242"
---
# <span data-ttu-id="a3a41-101">Remove-AzDataBoxEdgeUser</span><span class="sxs-lookup"><span data-stu-id="a3a41-101">Remove-AzDataBoxEdgeUser</span></span>

## <span data-ttu-id="a3a41-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a3a41-102">SYNOPSIS</span></span>
<span data-ttu-id="a3a41-103">Usuwa użytkownika z urządzenia.</span><span class="sxs-lookup"><span data-stu-id="a3a41-103">Removes a user on a device.</span></span>

## <span data-ttu-id="a3a41-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a3a41-104">SYNTAX</span></span>

### <span data-ttu-id="a3a41-105">DeleteByNameParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="a3a41-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a3a41-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a3a41-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxEdgeUser [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a3a41-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a3a41-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxEdgeUser [-InputObject] <PSDataBoxEdgeUser> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a3a41-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="a3a41-108">DESCRIPTION</span></span>
<span data-ttu-id="a3a41-109">Polecenie **cmdlet Remove-AzDataBoxEdgeUser** usuwa użytkownika z urządzenia z krawędzią pola danych.</span><span class="sxs-lookup"><span data-stu-id="a3a41-109">The **Remove-AzDataBoxEdgeUser** cmdlet removes a user on the Data Box Edge device.</span></span> <span data-ttu-id="a3a41-110">Obsługiwane jest tworzenie tylko użytkowników `Share` tego typu.</span><span class="sxs-lookup"><span data-stu-id="a3a41-110">Creation of only users of type `Share` is supported.</span></span>

## <span data-ttu-id="a3a41-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a3a41-111">EXAMPLES</span></span>

### <span data-ttu-id="a3a41-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a3a41-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxEdgeUser -ResourceGroupName resourceGroupName -DeviceName deviceName -Name username
```

## <span data-ttu-id="a3a41-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a3a41-113">PARAMETERS</span></span>

### <span data-ttu-id="a3a41-114">— AsJob</span><span class="sxs-lookup"><span data-stu-id="a3a41-114">-AsJob</span></span>
<span data-ttu-id="a3a41-115">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="a3a41-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a3a41-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3a41-116">-DefaultProfile</span></span>
<span data-ttu-id="a3a41-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="a3a41-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a3a41-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="a3a41-118">-DeviceName</span></span>
<span data-ttu-id="a3a41-119">Nazwa urządzenia</span><span class="sxs-lookup"><span data-stu-id="a3a41-119">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3a41-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a3a41-120">-InputObject</span></span>
<span data-ttu-id="a3a41-121">Obiekt Input</span><span class="sxs-lookup"><span data-stu-id="a3a41-121">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUser
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a3a41-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="a3a41-122">-Name</span></span>
<span data-ttu-id="a3a41-123">Nazwa użytkownika</span><span class="sxs-lookup"><span data-stu-id="a3a41-123">Username</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3a41-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a3a41-124">-PassThru</span></span>
<span data-ttu-id="a3a41-125">zwraca wartość prawda, jeśli pomyślnie</span><span class="sxs-lookup"><span data-stu-id="a3a41-125">returns true if successful</span></span>

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

### <span data-ttu-id="a3a41-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3a41-126">-ResourceGroupName</span></span>
<span data-ttu-id="a3a41-127">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="a3a41-127">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3a41-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a3a41-128">-ResourceId</span></span>
<span data-ttu-id="a3a41-129">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="a3a41-129">Azure ResourceId</span></span>

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

### <span data-ttu-id="a3a41-130">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a3a41-130">-Confirm</span></span>
<span data-ttu-id="a3a41-131">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="a3a41-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a3a41-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a3a41-132">-WhatIf</span></span>
<span data-ttu-id="a3a41-133">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a3a41-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a3a41-134">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="a3a41-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a3a41-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3a41-135">CommonParameters</span></span>
<span data-ttu-id="a3a41-136">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3a41-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3a41-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a3a41-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3a41-138">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a3a41-138">INPUTS</span></span>

### <span data-ttu-id="a3a41-139">System.String</span><span class="sxs-lookup"><span data-stu-id="a3a41-139">System.String</span></span>

### <span data-ttu-id="a3a41-140">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUser</span><span class="sxs-lookup"><span data-stu-id="a3a41-140">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUser</span></span>

## <span data-ttu-id="a3a41-141">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a3a41-141">OUTPUTS</span></span>

### <span data-ttu-id="a3a41-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="a3a41-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="a3a41-143">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a3a41-143">NOTES</span></span>

## <span data-ttu-id="a3a41-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a3a41-144">RELATED LINKS</span></span>
