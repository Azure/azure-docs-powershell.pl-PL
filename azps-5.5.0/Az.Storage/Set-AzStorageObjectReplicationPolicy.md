---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstorageobjectreplicationpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageObjectReplicationPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageObjectReplicationPolicy.md
ms.openlocfilehash: bf8d7aade5eeeafc2c3a78e4cdfed5df2d733006
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100241811"
---
# <span data-ttu-id="d79d9-101">Set-AzStorageObjectReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="d79d9-101">Set-AzStorageObjectReplicationPolicy</span></span>

## <span data-ttu-id="d79d9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d79d9-102">SYNOPSIS</span></span>
<span data-ttu-id="d79d9-103">Tworzy lub aktualizuje zasady replikacji określonych obiektów na koncie magazynu.</span><span class="sxs-lookup"><span data-stu-id="d79d9-103">Creates or updates the specified object replication policy in a Storage account.</span></span>

## <span data-ttu-id="d79d9-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d79d9-104">SYNTAX</span></span>

### <span data-ttu-id="d79d9-105">AccountName (Default)</span><span class="sxs-lookup"><span data-stu-id="d79d9-105">AccountName (Default)</span></span>
```
Set-AzStorageObjectReplicationPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-PolicyId <String>] -SourceAccount <String> [-DestinationAccount <String>]
 -Rule <PSObjectReplicationPolicyRule[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d79d9-106">PolicyObject</span><span class="sxs-lookup"><span data-stu-id="d79d9-106">PolicyObject</span></span>
```
Set-AzStorageObjectReplicationPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -InputObject <PSObjectReplicationPolicy> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d79d9-107">AccountObject</span><span class="sxs-lookup"><span data-stu-id="d79d9-107">AccountObject</span></span>
```
Set-AzStorageObjectReplicationPolicy -StorageAccount <PSStorageAccount> [-PolicyId <String>]
 -SourceAccount <String> [-DestinationAccount <String>] -Rule <PSObjectReplicationPolicyRule[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d79d9-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="d79d9-108">DESCRIPTION</span></span>
<span data-ttu-id="d79d9-109">Polecenie **cmdlet Set-AzStorageObjectReplicationPolicy** tworzy lub aktualizuje zasady replikacji określonych obiektów na koncie magazynu.</span><span class="sxs-lookup"><span data-stu-id="d79d9-109">The **Set-AzStorageObjectReplicationPolicy** cmdlet creates or updates the specified object replication policy in a Storage account.</span></span>

## <span data-ttu-id="d79d9-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d79d9-110">EXAMPLES</span></span>

### <span data-ttu-id="d79d9-111">Przykład 1. Konfigurowanie zasad replikacji obiektów zarówno dla konta docelowego, jak i źródłowego.</span><span class="sxs-lookup"><span data-stu-id="d79d9-111">Example 1: Set object replication policy to both destination and source account.</span></span>
```
PS C:\> $rule1 = New-AzStorageObjectReplicationPolicyRule -SourceContainer src1 -DestinationContainer dest1 

PS C:\> $rule2 = New-AzStorageObjectReplicationPolicyRule -SourceContainer src -DestinationContainer dest -MinCreationTime 2019-01-01T16:00:00Z -PrefixMatch a,abc,dd

PS C:\> $destPolicy = Set-AzStorageObjectReplicationPolicy -ResourceGroupName "myresourcegroup" -AccountName "mydestaccount" -PolicyId default -SourceAccount $srcAccountName  -Rule $rule1,$rule2

PS C:\> $destPolicy

ResourceGroupName StorageAccountName PolicyId                             EnabledTime SourceAccount   DestinationAccount Rules                                     
----------------- ------------------ --------                             ----------- -------------   ------------------ -----   
myresourcegroup   mydestaccount      56bfa11c-81ef-4f8d-b307-5e5386e16fba             mysourceaccount mydestaccount      [5fa8b1d6-4985-4abd-a0b3-ec4d07295a43,...]

PS C:\> Set-AzStorageObjectReplicationPolicy -ResourceGroupName "myresourcegroup" -AccountName "mysourceaccount" -InputObject $destPolicy

ResourceGroupName StorageAccountName PolicyId                             EnabledTime SourceAccount   DestinationAccount Rules                                     
----------------- ------------------ --------                             ----------- -------------   ------------------ -----                                     
myresourcegroup   mysourceaccount    56bfa11c-81ef-4f8d-b307-5e5386e16fba             mysourceaccount mydestaccount      [5fa8b1d6-4985-4abd-a0b3-ec4d07295a43,...]
```

<span data-ttu-id="d79d9-112">To polecenie ustawia zasady replikacji obiektów zarówno na konto docelowe, jak i źródłowe.</span><span class="sxs-lookup"><span data-stu-id="d79d9-112">This command sets object replication policy to both destination and source account.</span></span>
<span data-ttu-id="d79d9-113">Najpierw utwórz 2 reguły zasad replikacji obiektów i ustaw zasady z 2 regułami na konto docelowe.</span><span class="sxs-lookup"><span data-stu-id="d79d9-113">First create 2 object replication policy rules, and set policy with the 2 rules to destination account.</span></span> <span data-ttu-id="d79d9-114">Następnie ustaw zasady replikacji obiektów z konta docelowego na konto źródłowe.</span><span class="sxs-lookup"><span data-stu-id="d79d9-114">Then set the object replication policy from destination account to source account.</span></span>

## <span data-ttu-id="d79d9-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d79d9-115">PARAMETERS</span></span>

### <span data-ttu-id="d79d9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d79d9-116">-DefaultProfile</span></span>
<span data-ttu-id="d79d9-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="d79d9-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d79d9-118">-DestinationAccount</span><span class="sxs-lookup"><span data-stu-id="d79d9-118">-DestinationAccount</span></span>
<span data-ttu-id="d79d9-119">DestinationAccount zasad replikacji obiektów.</span><span class="sxs-lookup"><span data-stu-id="d79d9-119">Object Replication Policy DestinationAccount.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d79d9-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d79d9-120">-InputObject</span></span>
<span data-ttu-id="d79d9-121">Obiekt zasad replikacji obiektu ustawiony na określone konto.</span><span class="sxs-lookup"><span data-stu-id="d79d9-121">Object Replication Policy Object to Set to the specified Account.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSObjectReplicationPolicy
Parameter Sets: PolicyObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d79d9-122">-PolicyId</span><span class="sxs-lookup"><span data-stu-id="d79d9-122">-PolicyId</span></span>
<span data-ttu-id="d79d9-123">Identyfikator zasad replikacji obiektów. Powinien to być identyfikator GUID lub wartość "domyślna".</span><span class="sxs-lookup"><span data-stu-id="d79d9-123">Object Replication Policy Id. It should be a GUID or 'default'.</span></span>
<span data-ttu-id="d79d9-124">Jeśli nie zostanie włączona wartość PolicyId, użyje wartości "domyślne", co oznacza utworzenie nowych zasad, a identyfikator nowych zasad zostanie zwrócony w utworzonych zasadach.</span><span class="sxs-lookup"><span data-stu-id="d79d9-124">If not input the PolicyId, will use 'default', which means to create a new policy and the Id of the new policy will be returned in the created policy.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d79d9-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d79d9-125">-ResourceGroupName</span></span>
<span data-ttu-id="d79d9-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d79d9-126">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, PolicyObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d79d9-127">— reguła</span><span class="sxs-lookup"><span data-stu-id="d79d9-127">-Rule</span></span>
<span data-ttu-id="d79d9-128">Reguły zasad replikacji obiektów.</span><span class="sxs-lookup"><span data-stu-id="d79d9-128">Object Replication Policy Rules.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSObjectReplicationPolicyRule[]
Parameter Sets: AccountName, AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d79d9-129">-SourceAccount</span><span class="sxs-lookup"><span data-stu-id="d79d9-129">-SourceAccount</span></span>
<span data-ttu-id="d79d9-130">SourceAccount zasad replikacji obiektów.</span><span class="sxs-lookup"><span data-stu-id="d79d9-130">Object Replication Policy SourceAccount.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d79d9-131">— StorageAccount</span><span class="sxs-lookup"><span data-stu-id="d79d9-131">-StorageAccount</span></span>
<span data-ttu-id="d79d9-132">Obiekt konta magazynu</span><span class="sxs-lookup"><span data-stu-id="d79d9-132">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d79d9-133">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="d79d9-133">-StorageAccountName</span></span>
<span data-ttu-id="d79d9-134">Nazwa konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="d79d9-134">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, PolicyObject
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d79d9-135">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d79d9-135">-Confirm</span></span>
<span data-ttu-id="d79d9-136">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="d79d9-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d79d9-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d79d9-137">-WhatIf</span></span>
<span data-ttu-id="d79d9-138">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d79d9-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d79d9-139">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="d79d9-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d79d9-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d79d9-140">CommonParameters</span></span>
<span data-ttu-id="d79d9-141">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d79d9-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d79d9-142">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d79d9-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d79d9-143">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d79d9-143">INPUTS</span></span>

### <span data-ttu-id="d79d9-144">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d79d9-144">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="d79d9-145">Microsoft.Azure.Commands.Management.Storage.Models.PSObjectReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="d79d9-145">Microsoft.Azure.Commands.Management.Storage.Models.PSObjectReplicationPolicy</span></span>

## <span data-ttu-id="d79d9-146">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d79d9-146">OUTPUTS</span></span>

### <span data-ttu-id="d79d9-147">Microsoft.Azure.Commands.Management.Storage.Models.PSObjectReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="d79d9-147">Microsoft.Azure.Commands.Management.Storage.Models.PSObjectReplicationPolicy</span></span>

## <span data-ttu-id="d79d9-148">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d79d9-148">NOTES</span></span>

## <span data-ttu-id="d79d9-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d79d9-149">RELATED LINKS</span></span>
