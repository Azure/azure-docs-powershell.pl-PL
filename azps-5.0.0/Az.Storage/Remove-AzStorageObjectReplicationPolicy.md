---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstorageobjectreplicationpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageObjectReplicationPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageObjectReplicationPolicy.md
ms.openlocfilehash: 4c42fe6e612f30ab622a0a04498e5474f27690e9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94224770"
---
# <span data-ttu-id="d266c-101">Remove-AzStorageObjectReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="d266c-101">Remove-AzStorageObjectReplicationPolicy</span></span>

## <span data-ttu-id="d266c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d266c-102">SYNOPSIS</span></span>
<span data-ttu-id="d266c-103">Usuwa określone zasady replikacji obiektów z konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="d266c-103">Removes the specified object replication policy from a Storage account.</span></span>

## <span data-ttu-id="d266c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d266c-104">SYNTAX</span></span>

### <span data-ttu-id="d266c-105">AccountName (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="d266c-105">AccountName (Default)</span></span>
```
Remove-AzStorageObjectReplicationPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -PolicyId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d266c-106">AccountName</span><span class="sxs-lookup"><span data-stu-id="d266c-106">AccountObject</span></span>
```
Remove-AzStorageObjectReplicationPolicy -StorageAccount <PSStorageAccount> -PolicyId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d266c-107">Policyobject</span><span class="sxs-lookup"><span data-stu-id="d266c-107">PolicyObject</span></span>
```
Remove-AzStorageObjectReplicationPolicy -InputObject <PSObjectReplicationPolicy> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d266c-108">Opis</span><span class="sxs-lookup"><span data-stu-id="d266c-108">DESCRIPTION</span></span>
<span data-ttu-id="d266c-109">Polecenie cmdlet **Remove-AzStorageObjectReplicationPolicy** usuwa określone zasady replikacji obiektów z konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="d266c-109">The **Remove-AzStorageObjectReplicationPolicy** cmdlet removes the specified object replication policy from a Storage account.</span></span>

## <span data-ttu-id="d266c-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d266c-110">EXAMPLES</span></span>

### <span data-ttu-id="d266c-111">Przykład 1: usunięcie zasad replikacji obiektów z określonym policyId z konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="d266c-111">Example 1: Remove an object replication policy with specific policyId from a storage account.</span></span>
```
Remove-AzStorageObjectReplicationPolicy -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -PolicyId $policyId
```

<span data-ttu-id="d266c-112">To polecenie usuwa zasady replikacji obiektów z określonym policyId z konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="d266c-112">This command removes an object replication policy with specific policyId from a storage account.</span></span>

## <span data-ttu-id="d266c-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d266c-113">PARAMETERS</span></span>

### <span data-ttu-id="d266c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d266c-114">-DefaultProfile</span></span>
<span data-ttu-id="d266c-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d266c-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d266c-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="d266c-116">-InputObject</span></span>
<span data-ttu-id="d266c-117">Obiekt zasad replikacji obiektów do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="d266c-117">Object Replication Policy object to Delete.</span></span>

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

### <span data-ttu-id="d266c-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d266c-118">-PassThru</span></span>
<span data-ttu-id="d266c-119">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="d266c-119">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="d266c-120">-PolicyId</span><span class="sxs-lookup"><span data-stu-id="d266c-120">-PolicyId</span></span>
<span data-ttu-id="d266c-121">Identyfikator zasad replikacji obiektów.</span><span class="sxs-lookup"><span data-stu-id="d266c-121">Object Replication Policy Id.</span></span>

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

### <span data-ttu-id="d266c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d266c-122">-ResourceGroupName</span></span>
<span data-ttu-id="d266c-123">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d266c-123">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d266c-124">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="d266c-124">-StorageAccount</span></span>
<span data-ttu-id="d266c-125">Obiekt konta magazynu</span><span class="sxs-lookup"><span data-stu-id="d266c-125">Storage account object</span></span>

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

### <span data-ttu-id="d266c-126">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="d266c-126">-StorageAccountName</span></span>
<span data-ttu-id="d266c-127">Nazwa konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="d266c-127">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d266c-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d266c-128">-Confirm</span></span>
<span data-ttu-id="d266c-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d266c-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d266c-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d266c-130">-WhatIf</span></span>
<span data-ttu-id="d266c-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d266c-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d266c-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d266c-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d266c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d266c-133">CommonParameters</span></span>
<span data-ttu-id="d266c-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d266c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d266c-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d266c-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d266c-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d266c-136">INPUTS</span></span>

### <span data-ttu-id="d266c-137">Microsoft. Azure. Commands. Management. Storage. models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d266c-137">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="d266c-138">Microsoft. Azure. Commands. Management. Storage. models. PSObjectReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="d266c-138">Microsoft.Azure.Commands.Management.Storage.Models.PSObjectReplicationPolicy</span></span>

## <span data-ttu-id="d266c-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d266c-139">OUTPUTS</span></span>

### <span data-ttu-id="d266c-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d266c-140">System.Boolean</span></span>

## <span data-ttu-id="d266c-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d266c-141">NOTES</span></span>

## <span data-ttu-id="d266c-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d266c-142">RELATED LINKS</span></span>
