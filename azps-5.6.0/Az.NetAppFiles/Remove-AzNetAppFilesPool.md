---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/powershell/module/az.netappfiles/remove-aznetappfilespool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesPool.md
ms.openlocfilehash: a62e6093ec5cfdf7244ea83b2dccf07ad07308fb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101968321"
---
# <span data-ttu-id="2279d-101">Remove-AzNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="2279d-101">Remove-AzNetAppFilesPool</span></span>

## <span data-ttu-id="2279d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2279d-102">SYNOPSIS</span></span>
<span data-ttu-id="2279d-103">Usuwa pulę plików Azure NetApp Files (ANF).</span><span class="sxs-lookup"><span data-stu-id="2279d-103">Deletes an Azure NetApp Files (ANF) pool.</span></span>

## <span data-ttu-id="2279d-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="2279d-104">SYNTAX</span></span>

### <span data-ttu-id="2279d-105">ByFieldsParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="2279d-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesPool -ResourceGroupName <String> -AccountName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2279d-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2279d-106">ByParentObjectParameterSet</span></span>
```
Remove-AzNetAppFilesPool -Name <String> -AccountObject <PSNetAppFilesAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2279d-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2279d-107">ByResourceIdParameterSet</span></span>
```
Remove-AzNetAppFilesPool -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2279d-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2279d-108">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesPool -InputObject <PSNetAppFilesPool> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2279d-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="2279d-109">DESCRIPTION</span></span>
<span data-ttu-id="2279d-110">Polecenie **cmdlet Remove-AzNetAppFilesPool** usuwa pulę ANF.</span><span class="sxs-lookup"><span data-stu-id="2279d-110">The **Remove-AzNetAppFilesPool** cmdlet deletes an ANF pool.</span></span>

## <span data-ttu-id="2279d-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="2279d-111">EXAMPLES</span></span>

### <span data-ttu-id="2279d-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="2279d-112">Example 1</span></span>
```
PS C:\>Remove-AzNetAppFilesPool -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool"
```

<span data-ttu-id="2279d-113">To polecenie usuwa pulę ANF "MyAnfPool".</span><span class="sxs-lookup"><span data-stu-id="2279d-113">This command deletes the ANF pool "MyAnfPool".</span></span>

## <span data-ttu-id="2279d-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2279d-114">PARAMETERS</span></span>

### <span data-ttu-id="2279d-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="2279d-115">-AccountName</span></span>
<span data-ttu-id="2279d-116">Nazwa konta ANF</span><span class="sxs-lookup"><span data-stu-id="2279d-116">The name of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2279d-117">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="2279d-117">-AccountObject</span></span>
<span data-ttu-id="2279d-118">Obiekt konta zawierający pulę do usunięcia</span><span class="sxs-lookup"><span data-stu-id="2279d-118">The account object containing the pool to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2279d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2279d-119">-DefaultProfile</span></span>
<span data-ttu-id="2279d-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="2279d-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2279d-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2279d-121">-InputObject</span></span>
<span data-ttu-id="2279d-122">Obiekt puli do usunięcia</span><span class="sxs-lookup"><span data-stu-id="2279d-122">The pool object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2279d-123">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="2279d-123">-Name</span></span>
<span data-ttu-id="2279d-124">Nazwa puli ANF</span><span class="sxs-lookup"><span data-stu-id="2279d-124">The name of the ANF pool</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByParentObjectParameterSet
Aliases: PoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2279d-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2279d-125">-PassThru</span></span>
<span data-ttu-id="2279d-126">Zwracanie, czy określona pula została pomyślnie usunięta</span><span class="sxs-lookup"><span data-stu-id="2279d-126">Return whether the specified pool was successfully removed</span></span>

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

### <span data-ttu-id="2279d-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2279d-127">-ResourceGroupName</span></span>
<span data-ttu-id="2279d-128">Grupa zasobów puli ANF</span><span class="sxs-lookup"><span data-stu-id="2279d-128">The resource group of the ANF pool</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2279d-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2279d-129">-ResourceId</span></span>
<span data-ttu-id="2279d-130">Identyfikator zasobu puli ANF</span><span class="sxs-lookup"><span data-stu-id="2279d-130">The resource id of the ANF pool</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2279d-131">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2279d-131">-Confirm</span></span>
<span data-ttu-id="2279d-132">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="2279d-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2279d-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2279d-133">-WhatIf</span></span>
<span data-ttu-id="2279d-134">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2279d-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2279d-135">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="2279d-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2279d-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2279d-136">CommonParameters</span></span>
<span data-ttu-id="2279d-137">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2279d-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2279d-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2279d-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2279d-139">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2279d-139">INPUTS</span></span>

### <span data-ttu-id="2279d-140">System.String</span><span class="sxs-lookup"><span data-stu-id="2279d-140">System.String</span></span>

### <span data-ttu-id="2279d-141">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="2279d-141">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

### <span data-ttu-id="2279d-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="2279d-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="2279d-143">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2279d-143">OUTPUTS</span></span>

### <span data-ttu-id="2279d-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2279d-144">System.Boolean</span></span>

## <span data-ttu-id="2279d-145">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="2279d-145">NOTES</span></span>

## <span data-ttu-id="2279d-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2279d-146">RELATED LINKS</span></span>
