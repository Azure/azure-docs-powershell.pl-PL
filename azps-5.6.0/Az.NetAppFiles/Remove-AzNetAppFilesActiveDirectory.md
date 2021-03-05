---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/powershell/module/az.netappfiles/remove-aznetappfilesactivedirectory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesActiveDirectory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesActiveDirectory.md
ms.openlocfilehash: 9ab7607dd358e7c439539e99d44b263136f07cb4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101968362"
---
# <span data-ttu-id="d6b34-101">Remove-AzNetAppFilesActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="d6b34-101">Remove-AzNetAppFilesActiveDirectory</span></span>

## <span data-ttu-id="d6b34-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d6b34-102">SYNOPSIS</span></span>
<span data-ttu-id="d6b34-103">Usuwa konfigurację usługi Azure NetApp Files (ANF) w usłudze Active Directory.</span><span class="sxs-lookup"><span data-stu-id="d6b34-103">Deletes an Azure NetApp Files (ANF) active directory configuration.</span></span>

## <span data-ttu-id="d6b34-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d6b34-104">SYNTAX</span></span>

### <span data-ttu-id="d6b34-105">ByFieldsParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="d6b34-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesActiveDirectory -ResourceGroupName <String> -AccountName <String>
 -ActiveDirectoryId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d6b34-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d6b34-106">ByParentObjectParameterSet</span></span>
```
Remove-AzNetAppFilesActiveDirectory -ActiveDirectoryId <String> -AccountObject <PSNetAppFilesAccount>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d6b34-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d6b34-107">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesActiveDirectory -InputObject <PSNetAppFilesActiveDirectory> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d6b34-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="d6b34-108">DESCRIPTION</span></span>
<span data-ttu-id="d6b34-109">Polecenie **cmdlet Remove-AzNetAppFilesActiveDirectory** usuwa konfigurację usługi Active Directory ANF.</span><span class="sxs-lookup"><span data-stu-id="d6b34-109">The **Remove-AzNetAppFilesActiveDirectory** cmdlet deletes an ANF active directory configuration.</span></span>

## <span data-ttu-id="d6b34-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d6b34-110">EXAMPLES</span></span>

### <span data-ttu-id="d6b34-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d6b34-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzNetAppFilesActiveDirectory -ResourceGroupName "MyRG" -AccountName "MyAccount" -Name "MyADName"
```

<span data-ttu-id="d6b34-112">To polecenie usuwa nową konfigurację usługi Active Directory ANF o nazwie "MyADName".</span><span class="sxs-lookup"><span data-stu-id="d6b34-112">This command deletes the new ANF active directory configuration with a the name "MyADName".</span></span>

## <span data-ttu-id="d6b34-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d6b34-113">PARAMETERS</span></span>

### <span data-ttu-id="d6b34-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="d6b34-114">-AccountName</span></span>
<span data-ttu-id="d6b34-115">Nazwa konta ANF</span><span class="sxs-lookup"><span data-stu-id="d6b34-115">The name of the ANF account</span></span>

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

### <span data-ttu-id="d6b34-116">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="d6b34-116">-AccountObject</span></span>
<span data-ttu-id="d6b34-117">Konto obiektu usługi Active Directory</span><span class="sxs-lookup"><span data-stu-id="d6b34-117">The Account for the Active Directory object</span></span>

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

### <span data-ttu-id="d6b34-118">-ActiveDirectoryId</span><span class="sxs-lookup"><span data-stu-id="d6b34-118">-ActiveDirectoryId</span></span>
<span data-ttu-id="d6b34-119">Identyfikator usługi Active Directory ANF</span><span class="sxs-lookup"><span data-stu-id="d6b34-119">The ID of the ANF active directory</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6b34-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6b34-120">-DefaultProfile</span></span>
<span data-ttu-id="d6b34-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="d6b34-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d6b34-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d6b34-122">-InputObject</span></span>
<span data-ttu-id="d6b34-123">Obiekt usługi Active Directory do usunięcia</span><span class="sxs-lookup"><span data-stu-id="d6b34-123">The active directory object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d6b34-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d6b34-124">-PassThru</span></span>
<span data-ttu-id="d6b34-125">Zwracanie, czy określona usługa Active Directory została pomyślnie usunięta</span><span class="sxs-lookup"><span data-stu-id="d6b34-125">Return whether the specified Active Directory  was successfully removed</span></span>

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

### <span data-ttu-id="d6b34-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6b34-126">-ResourceGroupName</span></span>
<span data-ttu-id="d6b34-127">Grupa zasobów konta ANF</span><span class="sxs-lookup"><span data-stu-id="d6b34-127">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="d6b34-128">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d6b34-128">-Confirm</span></span>
<span data-ttu-id="d6b34-129">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="d6b34-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d6b34-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d6b34-130">-WhatIf</span></span>
<span data-ttu-id="d6b34-131">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d6b34-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d6b34-132">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="d6b34-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d6b34-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6b34-133">CommonParameters</span></span>
<span data-ttu-id="d6b34-134">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d6b34-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6b34-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d6b34-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6b34-136">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d6b34-136">INPUTS</span></span>

### <span data-ttu-id="d6b34-137">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="d6b34-137">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

### <span data-ttu-id="d6b34-138">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="d6b34-138">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory</span></span>

## <span data-ttu-id="d6b34-139">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d6b34-139">OUTPUTS</span></span>

### <span data-ttu-id="d6b34-140">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="d6b34-140">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory</span></span>

## <span data-ttu-id="d6b34-141">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d6b34-141">NOTES</span></span>

## <span data-ttu-id="d6b34-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d6b34-142">RELATED LINKS</span></span>
