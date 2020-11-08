---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/add-azrmstoragecontainerlegalhold
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Add-AzRmStorageContainerLegalHold.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Add-AzRmStorageContainerLegalHold.md
ms.openlocfilehash: 438aa207d28ca2a432d413f847d674d25bf55a42
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94064686"
---
# <span data-ttu-id="fc913-101">Add-AzRmStorageContainerLegalHold</span><span class="sxs-lookup"><span data-stu-id="fc913-101">Add-AzRmStorageContainerLegalHold</span></span>

## <span data-ttu-id="fc913-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fc913-102">SYNOPSIS</span></span>
<span data-ttu-id="fc913-103">Dodaje znaczniki blokady prawnej do kontenera obiektów BLOB magazynowania</span><span class="sxs-lookup"><span data-stu-id="fc913-103">Adds legal hold tags to a Storage blob container</span></span>

## <span data-ttu-id="fc913-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fc913-104">SYNTAX</span></span>

### <span data-ttu-id="fc913-105">AccountName (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="fc913-105">AccountName (Default)</span></span>
```
Add-AzRmStorageContainerLegalHold [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 -Tag <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fc913-106">AccountName</span><span class="sxs-lookup"><span data-stu-id="fc913-106">AccountObject</span></span>
```
Add-AzRmStorageContainerLegalHold -Name <String> -StorageAccount <PSStorageAccount> -Tag <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fc913-107">Containerobject</span><span class="sxs-lookup"><span data-stu-id="fc913-107">ContainerObject</span></span>
```
Add-AzRmStorageContainerLegalHold -Container <PSContainer> -Tag <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fc913-108">Opis</span><span class="sxs-lookup"><span data-stu-id="fc913-108">DESCRIPTION</span></span>
<span data-ttu-id="fc913-109">Polecenie cmdlet **Add-AzRmStorageContainerLegalHold** umożliwia dodanie znaczników dozwolonych do kontenera obiektów blob magazynu</span><span class="sxs-lookup"><span data-stu-id="fc913-109">The **Add-AzRmStorageContainerLegalHold** cmdlet adds legal hold tags to a Storage blob container</span></span>

## <span data-ttu-id="fc913-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fc913-110">EXAMPLES</span></span>

### <span data-ttu-id="fc913-111">Przykład 1. Dodaj Tagi blokady prawnej do kontenera obiektu blob magazynu z nazwą konta magazynu i nazwą kontenera</span><span class="sxs-lookup"><span data-stu-id="fc913-111">Example 1: Add legal hold tags to a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Add-AzRmStorageContainerLegalHold -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -Tag  tag1,tag2
```

<span data-ttu-id="fc913-112">To polecenie dodaje prawne znaczniki blokady do kontenera obiektu blob magazynu z nazwą konta magazynu i nazwą kontenera.</span><span class="sxs-lookup"><span data-stu-id="fc913-112">This command adds legal hold tags to a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="fc913-113">Przykład 2: Dodawanie znaczników z listy dozwolonych w kontenerze obiektów blob magazynu za pomocą obiektu konta magazynu i nazwy kontenera</span><span class="sxs-lookup"><span data-stu-id="fc913-113">Example 2: Add legal hold tags to a Storage blob container with Storage account object and container name</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Add-AzRmStorageContainerLegalHold -StorageAccount $accountObject -ContainerName "myContainer"  -Tag  tag1
```

<span data-ttu-id="fc913-114">To polecenie umożliwia dodanie znaczników w postaci prawnej do kontenera obiektu blob magazynu z obiektem konta magazynu i nazwą kontenera.</span><span class="sxs-lookup"><span data-stu-id="fc913-114">This command adds legal hold tags to a Storage blob container with Storage account object and container name.</span></span>

### <span data-ttu-id="fc913-115">Przykład 3: Dodawanie znaczników w postaci prawnej do wszystkich kontenerów obiektów blob magazynu na koncie magazynu z potokiem</span><span class="sxs-lookup"><span data-stu-id="fc913-115">Example 3: Add legal hold tags to all Storage blob containers in a Storage account with pipeline</span></span>
```
PS C:\>Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" | Add-AzRmStorageContainerLegalHold -Tag  tag1,tag2,tag3
```

<span data-ttu-id="fc913-116">To polecenie umożliwia dodanie znaczników w postaci prawnej do wszystkich kontenerów obiektów blob magazynu na koncie magazynu z potokiem.</span><span class="sxs-lookup"><span data-stu-id="fc913-116">This command adds legal hold tags to all Storage blob containers in a Storage account with pipeline.</span></span>

## <span data-ttu-id="fc913-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fc913-117">PARAMETERS</span></span>

### <span data-ttu-id="fc913-118">-Kontener</span><span class="sxs-lookup"><span data-stu-id="fc913-118">-Container</span></span>
<span data-ttu-id="fc913-119">Obiekt kontenera magazynu</span><span class="sxs-lookup"><span data-stu-id="fc913-119">Storage container object</span></span>

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

### <span data-ttu-id="fc913-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc913-120">-DefaultProfile</span></span>
<span data-ttu-id="fc913-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="fc913-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fc913-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="fc913-122">-Name</span></span>
<span data-ttu-id="fc913-123">Nazwa kontenera</span><span class="sxs-lookup"><span data-stu-id="fc913-123">Container Name</span></span>

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

### <span data-ttu-id="fc913-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc913-124">-ResourceGroupName</span></span>
<span data-ttu-id="fc913-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="fc913-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="fc913-126">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="fc913-126">-StorageAccount</span></span>
<span data-ttu-id="fc913-127">Obiekt konta magazynu</span><span class="sxs-lookup"><span data-stu-id="fc913-127">Storage account object</span></span>

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

### <span data-ttu-id="fc913-128">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="fc913-128">-StorageAccountName</span></span>
<span data-ttu-id="fc913-129">Nazwa konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="fc913-129">Storage Account Name.</span></span>

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

### <span data-ttu-id="fc913-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="fc913-130">-Tag</span></span>
<span data-ttu-id="fc913-131">Tagi LegalHold kontenera</span><span class="sxs-lookup"><span data-stu-id="fc913-131">Container LegalHold Tags</span></span>

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

### <span data-ttu-id="fc913-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="fc913-132">-Confirm</span></span>
<span data-ttu-id="fc913-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fc913-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fc913-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fc913-134">-WhatIf</span></span>
<span data-ttu-id="fc913-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fc913-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fc913-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="fc913-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fc913-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc913-137">CommonParameters</span></span>
<span data-ttu-id="fc913-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc913-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc913-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc913-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc913-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fc913-140">INPUTS</span></span>

### <span data-ttu-id="fc913-141">System. String</span><span class="sxs-lookup"><span data-stu-id="fc913-141">System.String</span></span>

### <span data-ttu-id="fc913-142">Microsoft. Azure. Commands. Management. Storage. models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="fc913-142">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="fc913-143">Microsoft. Azure. Commands. Management. Storage. models. PSContainer</span><span class="sxs-lookup"><span data-stu-id="fc913-143">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="fc913-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fc913-144">OUTPUTS</span></span>

### <span data-ttu-id="fc913-145">Microsoft. Azure. Commands. Management. Storage. models. PSLegalHold</span><span class="sxs-lookup"><span data-stu-id="fc913-145">Microsoft.Azure.Commands.Management.Storage.Models.PSLegalHold</span></span>

## <span data-ttu-id="fc913-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fc913-146">NOTES</span></span>

## <span data-ttu-id="fc913-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fc913-147">RELATED LINKS</span></span>
