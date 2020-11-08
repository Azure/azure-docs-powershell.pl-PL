---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstorageobjectreplicationpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageObjectReplicationPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageObjectReplicationPolicy.md
ms.openlocfilehash: bf8d7aade5eeeafc2c3a78e4cdfed5df2d733006
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94221020"
---
# <span data-ttu-id="c015a-101">Set-AzStorageObjectReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="c015a-101">Set-AzStorageObjectReplicationPolicy</span></span>

## <span data-ttu-id="c015a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c015a-102">SYNOPSIS</span></span>
<span data-ttu-id="c015a-103">Tworzy lub aktualizuje określone zasady replikacji obiektów na koncie magazynu.</span><span class="sxs-lookup"><span data-stu-id="c015a-103">Creates or updates the specified object replication policy in a Storage account.</span></span>

## <span data-ttu-id="c015a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c015a-104">SYNTAX</span></span>

### <span data-ttu-id="c015a-105">AccountName (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="c015a-105">AccountName (Default)</span></span>
```
Set-AzStorageObjectReplicationPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-PolicyId <String>] -SourceAccount <String> [-DestinationAccount <String>]
 -Rule <PSObjectReplicationPolicyRule[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c015a-106">Policyobject</span><span class="sxs-lookup"><span data-stu-id="c015a-106">PolicyObject</span></span>
```
Set-AzStorageObjectReplicationPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -InputObject <PSObjectReplicationPolicy> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c015a-107">AccountName</span><span class="sxs-lookup"><span data-stu-id="c015a-107">AccountObject</span></span>
```
Set-AzStorageObjectReplicationPolicy -StorageAccount <PSStorageAccount> [-PolicyId <String>]
 -SourceAccount <String> [-DestinationAccount <String>] -Rule <PSObjectReplicationPolicyRule[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c015a-108">Opis</span><span class="sxs-lookup"><span data-stu-id="c015a-108">DESCRIPTION</span></span>
<span data-ttu-id="c015a-109">Polecenie cmdlet **Set-AzStorageObjectReplicationPolicy** umożliwia utworzenie lub zaktualizowanie określonych zasad replikacji obiektów na koncie magazynu.</span><span class="sxs-lookup"><span data-stu-id="c015a-109">The **Set-AzStorageObjectReplicationPolicy** cmdlet creates or updates the specified object replication policy in a Storage account.</span></span>

## <span data-ttu-id="c015a-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c015a-110">EXAMPLES</span></span>

### <span data-ttu-id="c015a-111">Przykład 1: Ustawianie zasad replikacji obiektów zarówno na koncie docelowym, jak i źródłowym.</span><span class="sxs-lookup"><span data-stu-id="c015a-111">Example 1: Set object replication policy to both destination and source account.</span></span>
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

<span data-ttu-id="c015a-112">To polecenie ustawia zasady replikacji obiektów zarówno na miejsce docelowe, jak i konto źródłowe.</span><span class="sxs-lookup"><span data-stu-id="c015a-112">This command sets object replication policy to both destination and source account.</span></span>
<span data-ttu-id="c015a-113">Najpierw utwórz reguły replikacji 2-obiektowej i ustaw zasady za pomocą konta 2 reguł na koncie docelowym.</span><span class="sxs-lookup"><span data-stu-id="c015a-113">First create 2 object replication policy rules, and set policy with the 2 rules to destination account.</span></span> <span data-ttu-id="c015a-114">Następnie ustaw zasady replikacji obiektów z konta docelowego na konto źródłowe.</span><span class="sxs-lookup"><span data-stu-id="c015a-114">Then set the object replication policy from destination account to source account.</span></span>

## <span data-ttu-id="c015a-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c015a-115">PARAMETERS</span></span>

### <span data-ttu-id="c015a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c015a-116">-DefaultProfile</span></span>
<span data-ttu-id="c015a-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c015a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c015a-118">-DestinationAccount</span><span class="sxs-lookup"><span data-stu-id="c015a-118">-DestinationAccount</span></span>
<span data-ttu-id="c015a-119">DestinationAccount zasad replikacji obiektów.</span><span class="sxs-lookup"><span data-stu-id="c015a-119">Object Replication Policy DestinationAccount.</span></span>

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

### <span data-ttu-id="c015a-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="c015a-120">-InputObject</span></span>
<span data-ttu-id="c015a-121">Obiekt zasad replikacji obiektów, aby ustawić określone konto.</span><span class="sxs-lookup"><span data-stu-id="c015a-121">Object Replication Policy Object to Set to the specified Account.</span></span>

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

### <span data-ttu-id="c015a-122">-PolicyId</span><span class="sxs-lookup"><span data-stu-id="c015a-122">-PolicyId</span></span>
<span data-ttu-id="c015a-123">Identyfikator zasad replikacji obiektów. Powinien to być identyfikator GUID lub "domyślny".</span><span class="sxs-lookup"><span data-stu-id="c015a-123">Object Replication Policy Id. It should be a GUID or 'default'.</span></span>
<span data-ttu-id="c015a-124">Jeśli nie PolicyId, użyjemy "default", co oznacza, aby utworzyć nowe zasady, a identyfikator nowej zasady zostanie zwrócony w utworzonych zasadach.</span><span class="sxs-lookup"><span data-stu-id="c015a-124">If not input the PolicyId, will use 'default', which means to create a new policy and the Id of the new policy will be returned in the created policy.</span></span>

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

### <span data-ttu-id="c015a-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c015a-125">-ResourceGroupName</span></span>
<span data-ttu-id="c015a-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="c015a-126">Resource Group Name.</span></span>

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

### <span data-ttu-id="c015a-127">— Reguła</span><span class="sxs-lookup"><span data-stu-id="c015a-127">-Rule</span></span>
<span data-ttu-id="c015a-128">Reguły zasad replikacji obiektów.</span><span class="sxs-lookup"><span data-stu-id="c015a-128">Object Replication Policy Rules.</span></span>

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

### <span data-ttu-id="c015a-129">-SourceAccount</span><span class="sxs-lookup"><span data-stu-id="c015a-129">-SourceAccount</span></span>
<span data-ttu-id="c015a-130">SourceAccount zasad replikacji obiektów.</span><span class="sxs-lookup"><span data-stu-id="c015a-130">Object Replication Policy SourceAccount.</span></span>

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

### <span data-ttu-id="c015a-131">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="c015a-131">-StorageAccount</span></span>
<span data-ttu-id="c015a-132">Obiekt konta magazynu</span><span class="sxs-lookup"><span data-stu-id="c015a-132">Storage account object</span></span>

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

### <span data-ttu-id="c015a-133">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="c015a-133">-StorageAccountName</span></span>
<span data-ttu-id="c015a-134">Nazwa konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="c015a-134">Storage Account Name.</span></span>

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

### <span data-ttu-id="c015a-135">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c015a-135">-Confirm</span></span>
<span data-ttu-id="c015a-136">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c015a-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c015a-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c015a-137">-WhatIf</span></span>
<span data-ttu-id="c015a-138">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c015a-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c015a-139">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="c015a-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c015a-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c015a-140">CommonParameters</span></span>
<span data-ttu-id="c015a-141">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c015a-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c015a-142">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c015a-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c015a-143">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c015a-143">INPUTS</span></span>

### <span data-ttu-id="c015a-144">Microsoft. Azure. Commands. Management. Storage. models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c015a-144">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="c015a-145">Microsoft. Azure. Commands. Management. Storage. models. PSObjectReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="c015a-145">Microsoft.Azure.Commands.Management.Storage.Models.PSObjectReplicationPolicy</span></span>

## <span data-ttu-id="c015a-146">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c015a-146">OUTPUTS</span></span>

### <span data-ttu-id="c015a-147">Microsoft. Azure. Commands. Management. Storage. models. PSObjectReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="c015a-147">Microsoft.Azure.Commands.Management.Storage.Models.PSObjectReplicationPolicy</span></span>

## <span data-ttu-id="c015a-148">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c015a-148">NOTES</span></span>

## <span data-ttu-id="c015a-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c015a-149">RELATED LINKS</span></span>
