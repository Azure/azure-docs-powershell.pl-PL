---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/add-azrmstoragecontainerlegalhold
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Add-AzRmStorageContainerLegalHold.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Add-AzRmStorageContainerLegalHold.md
ms.openlocfilehash: 438aa207d28ca2a432d413f847d674d25bf55a42
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100187850"
---
# <span data-ttu-id="11e96-101">Add-AzRmStorageContainerLegalHold</span><span class="sxs-lookup"><span data-stu-id="11e96-101">Add-AzRmStorageContainerLegalHold</span></span>

## <span data-ttu-id="11e96-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="11e96-102">SYNOPSIS</span></span>
<span data-ttu-id="11e96-103">Dodaje tagi przechowywania prawnego do kontenera obiektów blob magazynu</span><span class="sxs-lookup"><span data-stu-id="11e96-103">Adds legal hold tags to a Storage blob container</span></span>

## <span data-ttu-id="11e96-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="11e96-104">SYNTAX</span></span>

### <span data-ttu-id="11e96-105">AccountName (Default)</span><span class="sxs-lookup"><span data-stu-id="11e96-105">AccountName (Default)</span></span>
```
Add-AzRmStorageContainerLegalHold [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 -Tag <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11e96-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="11e96-106">AccountObject</span></span>
```
Add-AzRmStorageContainerLegalHold -Name <String> -StorageAccount <PSStorageAccount> -Tag <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11e96-107">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="11e96-107">ContainerObject</span></span>
```
Add-AzRmStorageContainerLegalHold -Container <PSContainer> -Tag <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="11e96-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="11e96-108">DESCRIPTION</span></span>
<span data-ttu-id="11e96-109">Polecenie **cmdlet Add-AzRmStorageContainerLegalHold** dodaje tagi przechowywania prawnego do kontenera obiektów blob magazynu</span><span class="sxs-lookup"><span data-stu-id="11e96-109">The **Add-AzRmStorageContainerLegalHold** cmdlet adds legal hold tags to a Storage blob container</span></span>

## <span data-ttu-id="11e96-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="11e96-110">EXAMPLES</span></span>

### <span data-ttu-id="11e96-111">Przykład 1. Dodawanie tagów przechowywania prawnego do kontenera obiektów blob magazynu z nazwą konta magazynu i nazwą kontenera</span><span class="sxs-lookup"><span data-stu-id="11e96-111">Example 1: Add legal hold tags to a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Add-AzRmStorageContainerLegalHold -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -Tag  tag1,tag2
```

<span data-ttu-id="11e96-112">To polecenie dodaje tagi przechowywania prawnego do kontenera obiektów blob magazynu z nazwą konta magazynu i nazwą kontenera.</span><span class="sxs-lookup"><span data-stu-id="11e96-112">This command adds legal hold tags to a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="11e96-113">Przykład 2. Dodawanie tagów prawnych hold do kontenera obiektów blob magazynu z obiektem konta magazynu i nazwą kontenera</span><span class="sxs-lookup"><span data-stu-id="11e96-113">Example 2: Add legal hold tags to a Storage blob container with Storage account object and container name</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Add-AzRmStorageContainerLegalHold -StorageAccount $accountObject -ContainerName "myContainer"  -Tag  tag1
```

<span data-ttu-id="11e96-114">To polecenie dodaje tagi przechowywania prawnego do kontenera obiektów blob magazynu z obiektem konta magazynu i nazwą kontenera.</span><span class="sxs-lookup"><span data-stu-id="11e96-114">This command adds legal hold tags to a Storage blob container with Storage account object and container name.</span></span>

### <span data-ttu-id="11e96-115">Przykład 3. Dodawanie tagów prawnych hold do wszystkich kontenerów obiektów blob magazynu na koncie magazynu z potokiem</span><span class="sxs-lookup"><span data-stu-id="11e96-115">Example 3: Add legal hold tags to all Storage blob containers in a Storage account with pipeline</span></span>
```
PS C:\>Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" | Add-AzRmStorageContainerLegalHold -Tag  tag1,tag2,tag3
```

<span data-ttu-id="11e96-116">To polecenie dodaje tagi przechowywania ze względu na prawo do wszystkich kontenerów obiektów blob magazynu na koncie magazynu z potokiem.</span><span class="sxs-lookup"><span data-stu-id="11e96-116">This command adds legal hold tags to all Storage blob containers in a Storage account with pipeline.</span></span>

## <span data-ttu-id="11e96-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="11e96-117">PARAMETERS</span></span>

### <span data-ttu-id="11e96-118">— Kontener</span><span class="sxs-lookup"><span data-stu-id="11e96-118">-Container</span></span>
<span data-ttu-id="11e96-119">Obiekt kontener magazynu</span><span class="sxs-lookup"><span data-stu-id="11e96-119">Storage container object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSContainer
Parameter Sets: ContainerObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="11e96-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11e96-120">-DefaultProfile</span></span>
<span data-ttu-id="11e96-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="11e96-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="11e96-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="11e96-122">-Name</span></span>
<span data-ttu-id="11e96-123">Nazwa kontenera</span><span class="sxs-lookup"><span data-stu-id="11e96-123">Container Name</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountObject
Aliases: N, ContainerName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="11e96-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11e96-124">-ResourceGroupName</span></span>
<span data-ttu-id="11e96-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="11e96-125">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11e96-126">— StorageAccount</span><span class="sxs-lookup"><span data-stu-id="11e96-126">-StorageAccount</span></span>
<span data-ttu-id="11e96-127">Obiekt konta magazynu</span><span class="sxs-lookup"><span data-stu-id="11e96-127">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="11e96-128">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="11e96-128">-StorageAccountName</span></span>
<span data-ttu-id="11e96-129">Nazwa konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="11e96-129">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11e96-130">— Tag</span><span class="sxs-lookup"><span data-stu-id="11e96-130">-Tag</span></span>
<span data-ttu-id="11e96-131">Container LegalHold Tags</span><span class="sxs-lookup"><span data-stu-id="11e96-131">Container LegalHold Tags</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11e96-132">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="11e96-132">-Confirm</span></span>
<span data-ttu-id="11e96-133">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="11e96-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="11e96-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11e96-134">-WhatIf</span></span>
<span data-ttu-id="11e96-135">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="11e96-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="11e96-136">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="11e96-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="11e96-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11e96-137">CommonParameters</span></span>
<span data-ttu-id="11e96-138">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11e96-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11e96-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="11e96-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11e96-140">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="11e96-140">INPUTS</span></span>

### <span data-ttu-id="11e96-141">System.String</span><span class="sxs-lookup"><span data-stu-id="11e96-141">System.String</span></span>

### <span data-ttu-id="11e96-142">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="11e96-142">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="11e96-143">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span><span class="sxs-lookup"><span data-stu-id="11e96-143">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="11e96-144">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="11e96-144">OUTPUTS</span></span>

### <span data-ttu-id="11e96-145">Microsoft.Azure.Commands.Management.Storage.Models.PSLegalHold</span><span class="sxs-lookup"><span data-stu-id="11e96-145">Microsoft.Azure.Commands.Management.Storage.Models.PSLegalHold</span></span>

## <span data-ttu-id="11e96-146">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="11e96-146">NOTES</span></span>

## <span data-ttu-id="11e96-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="11e96-147">RELATED LINKS</span></span>
