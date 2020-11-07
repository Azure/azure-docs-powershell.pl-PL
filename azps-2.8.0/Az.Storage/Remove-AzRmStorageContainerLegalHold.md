---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azrmstoragecontainerlegalhold
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageContainerLegalHold.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageContainerLegalHold.md
ms.openlocfilehash: a7183498bba029a7b744a45bd34047926da4bf54
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93888130"
---
# <span data-ttu-id="58efe-101">Remove-AzRmStorageContainerLegalHold</span><span class="sxs-lookup"><span data-stu-id="58efe-101">Remove-AzRmStorageContainerLegalHold</span></span>

## <span data-ttu-id="58efe-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="58efe-102">SYNOPSIS</span></span>
<span data-ttu-id="58efe-103">Usuwa z kontenera obiektów blob magazynu prawnego Tagi</span><span class="sxs-lookup"><span data-stu-id="58efe-103">Removes legal hold tags from a Storage blob container</span></span>

## <span data-ttu-id="58efe-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="58efe-104">SYNTAX</span></span>

### <span data-ttu-id="58efe-105">AccountName (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="58efe-105">AccountName (Default)</span></span>
```
Remove-AzRmStorageContainerLegalHold [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -Name <String> -Tag <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="58efe-106">AccountName</span><span class="sxs-lookup"><span data-stu-id="58efe-106">AccountObject</span></span>
```
Remove-AzRmStorageContainerLegalHold -Name <String> -StorageAccount <PSStorageAccount> -Tag <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="58efe-107">Containerobject</span><span class="sxs-lookup"><span data-stu-id="58efe-107">ContainerObject</span></span>
```
Remove-AzRmStorageContainerLegalHold -Container <PSContainer> -Tag <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="58efe-108">Opis</span><span class="sxs-lookup"><span data-stu-id="58efe-108">DESCRIPTION</span></span>
<span data-ttu-id="58efe-109">Polecenie cmdlet **Remove-AzRmStorageContainerLegalHold** usuwa z kontenera obiektów blob magazynu prawnego Tagi</span><span class="sxs-lookup"><span data-stu-id="58efe-109">The **Remove-AzRmStorageContainerLegalHold** cmdlet removes legal hold tags from a Storage blob container</span></span>

## <span data-ttu-id="58efe-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="58efe-110">EXAMPLES</span></span>

### <span data-ttu-id="58efe-111">Przykład 1: usuwanie prawnych znaczników blokad z kontenera obiektu blob magazynu z nazwą konta magazynu i nazwą kontenera</span><span class="sxs-lookup"><span data-stu-id="58efe-111">Example 1: Remove legal hold tags from a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Remove-AzRmStorageContainerLegalHold -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -Tag  tag1
```

<span data-ttu-id="58efe-112">To polecenie usuwa prawne znaczniki blokad z kontenera obiektu blob magazynu z nazwą konta magazynu i nazwą kontenera.</span><span class="sxs-lookup"><span data-stu-id="58efe-112">This command removes legal hold tags from a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="58efe-113">Przykład 2: usuwanie dozwolonych znaczników blokad z kontenera obiektu BLOB magazynowania z obiektem konta magazynu i nazwą kontenera</span><span class="sxs-lookup"><span data-stu-id="58efe-113">Example 2: Remove legal hold tags from a Storage blob container with Storage account object and container name</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Remove-AzRmStorageContainerLegalHold -StorageAccount $accountObject -ContainerName "myContainer"  -Tag  tag1,tag2
```

<span data-ttu-id="58efe-114">To polecenie usuwa prawne znaczniki blokad z kontenera obiektu blob magazynu z obiektem konta magazynu i nazwą kontenera.</span><span class="sxs-lookup"><span data-stu-id="58efe-114">This command removes legal hold tags from a Storage blob container with Storage account object and container name.</span></span>

### <span data-ttu-id="58efe-115">Przykład 3: usuwanie prawnych znaczników blokad ze wszystkich kontenerów obiektów blob magazynu na koncie magazynu z potokiem</span><span class="sxs-lookup"><span data-stu-id="58efe-115">Example 3: Remove legal hold tags from all Storage blob containers in a Storage account with pipeline</span></span>
```
PS C:\>Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" | Remove-AzRmStorageContainerLegalHold -Tag  tag1
```

<span data-ttu-id="58efe-116">To polecenie usuwa prawne znaczniki blokad ze wszystkich kontenerów obiektów blob magazynu na koncie magazynu z potokiem.</span><span class="sxs-lookup"><span data-stu-id="58efe-116">This command removes legal hold tags from all Storage blob containers in a Storage account with pipeline.</span></span>

## <span data-ttu-id="58efe-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="58efe-117">PARAMETERS</span></span>

### <span data-ttu-id="58efe-118">-Kontener</span><span class="sxs-lookup"><span data-stu-id="58efe-118">-Container</span></span>
<span data-ttu-id="58efe-119">Obiekt kontenera magazynu</span><span class="sxs-lookup"><span data-stu-id="58efe-119">Storage container object</span></span>

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

### <span data-ttu-id="58efe-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58efe-120">-DefaultProfile</span></span>
<span data-ttu-id="58efe-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="58efe-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="58efe-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="58efe-122">-Name</span></span>
<span data-ttu-id="58efe-123">Nazwa kontenera</span><span class="sxs-lookup"><span data-stu-id="58efe-123">Container Name</span></span>

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

### <span data-ttu-id="58efe-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58efe-124">-ResourceGroupName</span></span>
<span data-ttu-id="58efe-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="58efe-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="58efe-126">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="58efe-126">-StorageAccount</span></span>
<span data-ttu-id="58efe-127">Obiekt konta magazynu</span><span class="sxs-lookup"><span data-stu-id="58efe-127">Storage account object</span></span>

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

### <span data-ttu-id="58efe-128">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="58efe-128">-StorageAccountName</span></span>
<span data-ttu-id="58efe-129">Nazwa konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="58efe-129">Storage Account Name.</span></span>

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

### <span data-ttu-id="58efe-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="58efe-130">-Tag</span></span>
<span data-ttu-id="58efe-131">Tagi LegalHold kontenera</span><span class="sxs-lookup"><span data-stu-id="58efe-131">Container LegalHold Tags</span></span>

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

### <span data-ttu-id="58efe-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="58efe-132">-Confirm</span></span>
<span data-ttu-id="58efe-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="58efe-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="58efe-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="58efe-134">-WhatIf</span></span>
<span data-ttu-id="58efe-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="58efe-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="58efe-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="58efe-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="58efe-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58efe-137">CommonParameters</span></span>
<span data-ttu-id="58efe-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58efe-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58efe-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="58efe-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58efe-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="58efe-140">INPUTS</span></span>

### <span data-ttu-id="58efe-141">System. String</span><span class="sxs-lookup"><span data-stu-id="58efe-141">System.String</span></span>

### <span data-ttu-id="58efe-142">Microsoft. Azure. Commands. Management. Storage. models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="58efe-142">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="58efe-143">Microsoft. Azure. Commands. Management. Storage. models. PSContainer</span><span class="sxs-lookup"><span data-stu-id="58efe-143">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="58efe-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="58efe-144">OUTPUTS</span></span>

### <span data-ttu-id="58efe-145">Microsoft. Azure. Commands. Management. Storage. models. PSLegalHold</span><span class="sxs-lookup"><span data-stu-id="58efe-145">Microsoft.Azure.Commands.Management.Storage.Models.PSLegalHold</span></span>

## <span data-ttu-id="58efe-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="58efe-146">NOTES</span></span>

## <span data-ttu-id="58efe-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="58efe-147">RELATED LINKS</span></span>
