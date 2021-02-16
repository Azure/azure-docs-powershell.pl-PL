---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/remove-azdataboxedgestorageaccountcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeStorageAccountCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeStorageAccountCredential.md
ms.openlocfilehash: 00cfc136465cc250d068344158d66f98dc6e0704
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100188658"
---
# <span data-ttu-id="6add3-101">Remove-AzDataBoxEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="6add3-101">Remove-AzDataBoxEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="6add3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6add3-102">SYNOPSIS</span></span>
<span data-ttu-id="6add3-103">Usuwa poświadczenia konta magazynu dla urządzenia.</span><span class="sxs-lookup"><span data-stu-id="6add3-103">Removes a storage account credential for a device.</span></span>

## <span data-ttu-id="6add3-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="6add3-104">SYNTAX</span></span>

### <span data-ttu-id="6add3-105">DeleteByNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="6add3-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxEdgeStorageAccountCredential [-ResourceGroupName] <String> [-DeviceName] <String>
 [-Name] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6add3-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6add3-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxEdgeStorageAccountCredential [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6add3-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6add3-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxEdgeStorageAccountCredential [-InputObject] <PSDataBoxEdgeStorageAccountCredential> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6add3-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="6add3-108">DESCRIPTION</span></span>
<span data-ttu-id="6add3-109">Polecenie **cmdlet Remove-AzDataBoxEdgeStorageAccountCredential** usuwa poświadczenia konta magazynu dla urządzenia z krawędzią pola danych.</span><span class="sxs-lookup"><span data-stu-id="6add3-109">The **Remove-AzDataBoxEdgeStorageAccountCredential** cmdlet removes the storage account credential for a Data Box Edge device.</span></span>

## <span data-ttu-id="6add3-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="6add3-110">EXAMPLES</span></span>

### <span data-ttu-id="6add3-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="6add3-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxEdgeStorageAccountCredential ResourceGroupName resourceGroupName -DeviceName deviceName -Name storageAccountCredentialName
```

## <span data-ttu-id="6add3-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6add3-112">PARAMETERS</span></span>

### <span data-ttu-id="6add3-113">— AsJob</span><span class="sxs-lookup"><span data-stu-id="6add3-113">-AsJob</span></span>
<span data-ttu-id="6add3-114">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="6add3-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6add3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6add3-115">-DefaultProfile</span></span>
<span data-ttu-id="6add3-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="6add3-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6add3-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="6add3-117">-DeviceName</span></span>
<span data-ttu-id="6add3-118">Nazwa urządzenia</span><span class="sxs-lookup"><span data-stu-id="6add3-118">Device Name</span></span>

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

### <span data-ttu-id="6add3-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6add3-119">-InputObject</span></span>
<span data-ttu-id="6add3-120">Obiekt Input</span><span class="sxs-lookup"><span data-stu-id="6add3-120">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6add3-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="6add3-121">-Name</span></span>
<span data-ttu-id="6add3-122">Nazwa konta miejsca do magazynowania, które ma zostać użyte</span><span class="sxs-lookup"><span data-stu-id="6add3-122">Name of the storage account to be used</span></span>

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

### <span data-ttu-id="6add3-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6add3-123">-PassThru</span></span>
<span data-ttu-id="6add3-124">zwraca wartość prawda, jeśli pomyślnie</span><span class="sxs-lookup"><span data-stu-id="6add3-124">returns true if successful</span></span>

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

### <span data-ttu-id="6add3-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6add3-125">-ResourceGroupName</span></span>
<span data-ttu-id="6add3-126">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="6add3-126">Resource Group Name</span></span>

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

### <span data-ttu-id="6add3-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6add3-127">-ResourceId</span></span>
<span data-ttu-id="6add3-128">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="6add3-128">Azure ResourceId</span></span>

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

### <span data-ttu-id="6add3-129">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6add3-129">-Confirm</span></span>
<span data-ttu-id="6add3-130">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="6add3-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6add3-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6add3-131">-WhatIf</span></span>
<span data-ttu-id="6add3-132">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6add3-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6add3-133">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="6add3-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6add3-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6add3-134">CommonParameters</span></span>
<span data-ttu-id="6add3-135">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6add3-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6add3-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6add3-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6add3-137">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6add3-137">INPUTS</span></span>

### <span data-ttu-id="6add3-138">System.String</span><span class="sxs-lookup"><span data-stu-id="6add3-138">System.String</span></span>

### <span data-ttu-id="6add3-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="6add3-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="6add3-140">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6add3-140">OUTPUTS</span></span>

### <span data-ttu-id="6add3-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="6add3-141">System.Boolean</span></span>

## <span data-ttu-id="6add3-142">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="6add3-142">NOTES</span></span>

## <span data-ttu-id="6add3-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6add3-143">RELATED LINKS</span></span>
