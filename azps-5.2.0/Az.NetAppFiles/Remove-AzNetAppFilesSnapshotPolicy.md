---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/remove-aznetappfilessnapshotpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesSnapshotPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesSnapshotPolicy.md
ms.openlocfilehash: 6ea65189969e38359bb6d4345ea4c47963f9eddf
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98325925"
---
# <span data-ttu-id="98c9b-101">Remove-AzNetAppFilesSnapshotPolicy</span><span class="sxs-lookup"><span data-stu-id="98c9b-101">Remove-AzNetAppFilesSnapshotPolicy</span></span>

## <span data-ttu-id="98c9b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="98c9b-102">SYNOPSIS</span></span>
<span data-ttu-id="98c9b-103">Usuwa zasady migawki plików usługi Azure NetApp (ANF).</span><span class="sxs-lookup"><span data-stu-id="98c9b-103">Deletes an Azure NetApp Files (ANF) snapshot policy.</span></span>

## <span data-ttu-id="98c9b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="98c9b-104">SYNTAX</span></span>

### <span data-ttu-id="98c9b-105">ByFieldsParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="98c9b-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesSnapshotPolicy -ResourceGroupName <String> -AccountName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="98c9b-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="98c9b-106">ByParentObjectParameterSet</span></span>
```
Remove-AzNetAppFilesSnapshotPolicy -Name <String> -AccountObject <PSNetAppFilesAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="98c9b-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="98c9b-107">ByResourceIdParameterSet</span></span>
```
Remove-AzNetAppFilesSnapshotPolicy -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="98c9b-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="98c9b-108">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesSnapshotPolicy -InputObject <PSNetAppFilesSnapshotPolicy> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="98c9b-109">Opis</span><span class="sxs-lookup"><span data-stu-id="98c9b-109">DESCRIPTION</span></span>
<span data-ttu-id="98c9b-110">Polecenie cmdlet **Remove-AzNetAppFilesSnapshotPolicy** usuwa ANF migawki.</span><span class="sxs-lookup"><span data-stu-id="98c9b-110">The **Remove-AzNetAppFilesSnapshotPolicy** cmdlet deletes an ANF snapshot policy.</span></span>

## <span data-ttu-id="98c9b-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="98c9b-111">EXAMPLES</span></span>

### <span data-ttu-id="98c9b-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="98c9b-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzNetAppFilesSnapshotPolicy -ResourceGroupName "MyRG" -AccountName "MyAccount" -Name "MySnapshotPolicy"
```

<span data-ttu-id="98c9b-113">To polecenie usuwa nowe zasady ANF kopii zapasowej z nazwą "MyBackupPolicy" dla konta "Moje konto".</span><span class="sxs-lookup"><span data-stu-id="98c9b-113">This command deletes the new ANF backup policy with a the name "MyBackupPolicy" for account "MyAccount".</span></span>

## <span data-ttu-id="98c9b-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="98c9b-114">PARAMETERS</span></span>

### <span data-ttu-id="98c9b-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="98c9b-115">-AccountName</span></span>
<span data-ttu-id="98c9b-116">Nazwa konta usługi ANF</span><span class="sxs-lookup"><span data-stu-id="98c9b-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="98c9b-117">-Accountobject</span><span class="sxs-lookup"><span data-stu-id="98c9b-117">-AccountObject</span></span>
<span data-ttu-id="98c9b-118">Konto nowego obiektu zasad migawki</span><span class="sxs-lookup"><span data-stu-id="98c9b-118">The Account for the new Snapshot Policy object</span></span>

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

### <span data-ttu-id="98c9b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98c9b-119">-DefaultProfile</span></span>
<span data-ttu-id="98c9b-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="98c9b-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="98c9b-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="98c9b-121">-InputObject</span></span>
<span data-ttu-id="98c9b-122">Obiekt SnapshotPolicy do usunięcia</span><span class="sxs-lookup"><span data-stu-id="98c9b-122">The SnapshotPolicy object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshotPolicy
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="98c9b-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="98c9b-123">-Name</span></span>
<span data-ttu-id="98c9b-124">Nazwa zasady migawki ANF</span><span class="sxs-lookup"><span data-stu-id="98c9b-124">The name of the ANF snapshot policy</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByParentObjectParameterSet
Aliases: SnapshotPolicyName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98c9b-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="98c9b-125">-PassThru</span></span>
<span data-ttu-id="98c9b-126">Zwracanie, czy określone konto zostało pomyślnie usunięte</span><span class="sxs-lookup"><span data-stu-id="98c9b-126">Return whether the specified account was successfully removed</span></span>

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

### <span data-ttu-id="98c9b-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="98c9b-127">-ResourceGroupName</span></span>
<span data-ttu-id="98c9b-128">Grupa zasobów konta ANF</span><span class="sxs-lookup"><span data-stu-id="98c9b-128">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="98c9b-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="98c9b-129">-ResourceId</span></span>
<span data-ttu-id="98c9b-130">Identyfikator zasobu w zasadach migawki ANF</span><span class="sxs-lookup"><span data-stu-id="98c9b-130">The resource id of the ANF Snapshot Policy</span></span>

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

### <span data-ttu-id="98c9b-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="98c9b-131">-Confirm</span></span>
<span data-ttu-id="98c9b-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="98c9b-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="98c9b-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="98c9b-133">-WhatIf</span></span>
<span data-ttu-id="98c9b-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="98c9b-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="98c9b-135">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="98c9b-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="98c9b-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98c9b-136">CommonParameters</span></span>
<span data-ttu-id="98c9b-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="98c9b-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98c9b-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="98c9b-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98c9b-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="98c9b-139">INPUTS</span></span>

### <span data-ttu-id="98c9b-140">System. String</span><span class="sxs-lookup"><span data-stu-id="98c9b-140">System.String</span></span>

### <span data-ttu-id="98c9b-141">Microsoft. Azure. Commands. NetAppFiles. models. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="98c9b-141">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

### <span data-ttu-id="98c9b-142">Microsoft. Azure. Commands. NetAppFiles. models. PSNetAppFilesSnapshotPolicy</span><span class="sxs-lookup"><span data-stu-id="98c9b-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshotPolicy</span></span>

## <span data-ttu-id="98c9b-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="98c9b-143">OUTPUTS</span></span>

### <span data-ttu-id="98c9b-144">Microsoft. Azure. Commands. NetAppFiles. models. PSNetAppFilesSnapshotPolicy</span><span class="sxs-lookup"><span data-stu-id="98c9b-144">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshotPolicy</span></span>

## <span data-ttu-id="98c9b-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="98c9b-145">NOTES</span></span>

## <span data-ttu-id="98c9b-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="98c9b-146">RELATED LINKS</span></span>
