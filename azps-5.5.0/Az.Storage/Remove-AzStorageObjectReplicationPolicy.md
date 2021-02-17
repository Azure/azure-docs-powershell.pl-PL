---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstorageobjectreplicationpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageObjectReplicationPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageObjectReplicationPolicy.md
ms.openlocfilehash: 4c42fe6e612f30ab622a0a04498e5474f27690e9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100198418"
---
# <span data-ttu-id="3cc35-101">Remove-AzStorageObjectReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="3cc35-101">Remove-AzStorageObjectReplicationPolicy</span></span>

## <span data-ttu-id="3cc35-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3cc35-102">SYNOPSIS</span></span>
<span data-ttu-id="3cc35-103">Usuwa określone zasady replikacji obiektów z konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="3cc35-103">Removes the specified object replication policy from a Storage account.</span></span>

## <span data-ttu-id="3cc35-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="3cc35-104">SYNTAX</span></span>

### <span data-ttu-id="3cc35-105">AccountName (Default)</span><span class="sxs-lookup"><span data-stu-id="3cc35-105">AccountName (Default)</span></span>
```
Remove-AzStorageObjectReplicationPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -PolicyId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3cc35-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="3cc35-106">AccountObject</span></span>
```
Remove-AzStorageObjectReplicationPolicy -StorageAccount <PSStorageAccount> -PolicyId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3cc35-107">PolicyObject</span><span class="sxs-lookup"><span data-stu-id="3cc35-107">PolicyObject</span></span>
```
Remove-AzStorageObjectReplicationPolicy -InputObject <PSObjectReplicationPolicy> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3cc35-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="3cc35-108">DESCRIPTION</span></span>
<span data-ttu-id="3cc35-109">Polecenie **cmdlet Remove-AzStorageObjectReplicationPolicy** usuwa zasady replikacji określonego obiektu z konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="3cc35-109">The **Remove-AzStorageObjectReplicationPolicy** cmdlet removes the specified object replication policy from a Storage account.</span></span>

## <span data-ttu-id="3cc35-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="3cc35-110">EXAMPLES</span></span>

### <span data-ttu-id="3cc35-111">Przykład 1. Usunięcie zasad replikacji obiektów z określonymi identyfikatorami zasad z konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="3cc35-111">Example 1: Remove an object replication policy with specific policyId from a storage account.</span></span>
```
Remove-AzStorageObjectReplicationPolicy -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -PolicyId $policyId
```

<span data-ttu-id="3cc35-112">To polecenie usuwa z konta magazynu zasady replikacji obiektów o określonych identyfikatorach zasad.</span><span class="sxs-lookup"><span data-stu-id="3cc35-112">This command removes an object replication policy with specific policyId from a storage account.</span></span>

## <span data-ttu-id="3cc35-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3cc35-113">PARAMETERS</span></span>

### <span data-ttu-id="3cc35-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3cc35-114">-DefaultProfile</span></span>
<span data-ttu-id="3cc35-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="3cc35-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3cc35-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3cc35-116">-InputObject</span></span>
<span data-ttu-id="3cc35-117">Obiekt zasad replikacji obiektów do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="3cc35-117">Object Replication Policy object to Delete.</span></span>

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

### <span data-ttu-id="3cc35-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3cc35-118">-PassThru</span></span>
<span data-ttu-id="3cc35-119">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="3cc35-119">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="3cc35-120">-PolicyId</span><span class="sxs-lookup"><span data-stu-id="3cc35-120">-PolicyId</span></span>
<span data-ttu-id="3cc35-121">Identyfikator zasad replikacji obiektów.</span><span class="sxs-lookup"><span data-stu-id="3cc35-121">Object Replication Policy Id.</span></span>

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

### <span data-ttu-id="3cc35-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3cc35-122">-ResourceGroupName</span></span>
<span data-ttu-id="3cc35-123">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="3cc35-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="3cc35-124">— StorageAccount</span><span class="sxs-lookup"><span data-stu-id="3cc35-124">-StorageAccount</span></span>
<span data-ttu-id="3cc35-125">Obiekt konta magazynu</span><span class="sxs-lookup"><span data-stu-id="3cc35-125">Storage account object</span></span>

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

### <span data-ttu-id="3cc35-126">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="3cc35-126">-StorageAccountName</span></span>
<span data-ttu-id="3cc35-127">Nazwa konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="3cc35-127">Storage Account Name.</span></span>

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

### <span data-ttu-id="3cc35-128">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3cc35-128">-Confirm</span></span>
<span data-ttu-id="3cc35-129">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="3cc35-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3cc35-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3cc35-130">-WhatIf</span></span>
<span data-ttu-id="3cc35-131">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3cc35-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3cc35-132">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="3cc35-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3cc35-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3cc35-133">CommonParameters</span></span>
<span data-ttu-id="3cc35-134">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3cc35-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3cc35-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3cc35-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3cc35-136">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3cc35-136">INPUTS</span></span>

### <span data-ttu-id="3cc35-137">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3cc35-137">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="3cc35-138">Microsoft.Azure.Commands.Management.Storage.Models.PSObjectReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="3cc35-138">Microsoft.Azure.Commands.Management.Storage.Models.PSObjectReplicationPolicy</span></span>

## <span data-ttu-id="3cc35-139">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3cc35-139">OUTPUTS</span></span>

### <span data-ttu-id="3cc35-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="3cc35-140">System.Boolean</span></span>

## <span data-ttu-id="3cc35-141">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="3cc35-141">NOTES</span></span>

## <span data-ttu-id="3cc35-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3cc35-142">RELATED LINKS</span></span>
