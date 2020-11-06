---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/add-azurermstoragecontainerlegalhold
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Add-AzureRmStorageContainerLegalHold.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Add-AzureRmStorageContainerLegalHold.md
ms.openlocfilehash: 465a40e384e5ea7240e0ced2a010c88529feb2f5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525965"
---
# <span data-ttu-id="37c7f-101">Add-AzureRmStorageContainerLegalHold</span><span class="sxs-lookup"><span data-stu-id="37c7f-101">Add-AzureRmStorageContainerLegalHold</span></span>

## <span data-ttu-id="37c7f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="37c7f-102">SYNOPSIS</span></span>
<span data-ttu-id="37c7f-103">Dodaje znaczniki blokady prawnej do kontenera obiektów BLOB magazynowania</span><span class="sxs-lookup"><span data-stu-id="37c7f-103">Adds legal hold tags to a Storage blob container</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="37c7f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="37c7f-104">SYNTAX</span></span>

### <span data-ttu-id="37c7f-105">AccountName (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="37c7f-105">AccountName (Default)</span></span>
```
Add-AzureRmStorageContainerLegalHold [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -Name <String> -Tag <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="37c7f-106">AccountName</span><span class="sxs-lookup"><span data-stu-id="37c7f-106">AccountObject</span></span>
```
Add-AzureRmStorageContainerLegalHold -Name <String> -StorageAccount <PSStorageAccount> -Tag <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="37c7f-107">Containerobject</span><span class="sxs-lookup"><span data-stu-id="37c7f-107">ContainerObject</span></span>
```
Add-AzureRmStorageContainerLegalHold -Container <PSContainer> -Tag <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="37c7f-108">Opis</span><span class="sxs-lookup"><span data-stu-id="37c7f-108">DESCRIPTION</span></span>
<span data-ttu-id="37c7f-109">Polecenie cmdlet **Add-AzureRmStorageContainerLegalHold** umożliwia dodanie znaczników dozwolonych do kontenera obiektów blob magazynu</span><span class="sxs-lookup"><span data-stu-id="37c7f-109">The **Add-AzureRmStorageContainerLegalHold** cmdlet adds legal hold tags to a Storage blob container</span></span>

## <span data-ttu-id="37c7f-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="37c7f-110">EXAMPLES</span></span>

### <span data-ttu-id="37c7f-111">Przykład 1. Dodaj Tagi blokady prawnej do kontenera obiektu blob magazynu z nazwą konta magazynu i nazwą kontenera</span><span class="sxs-lookup"><span data-stu-id="37c7f-111">Example 1: Add legal hold tags to a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Add-AzureRmStorageContainerLegalHold -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -Tag  tag1,tag2 
```

<span data-ttu-id="37c7f-112">To polecenie dodaje prawne znaczniki blokady do kontenera obiektu blob magazynu z nazwą konta magazynu i nazwą kontenera.</span><span class="sxs-lookup"><span data-stu-id="37c7f-112">This command adds legal hold tags to a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="37c7f-113">Przykład 2: Dodawanie znaczników z listy dozwolonych w kontenerze obiektów blob magazynu za pomocą obiektu konta magazynu i nazwy kontenera</span><span class="sxs-lookup"><span data-stu-id="37c7f-113">Example 2: Add legal hold tags to a Storage blob container with Storage account object and container name</span></span>
```
PS C:\>$accountObject = Get-AzureRmStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Add-AzureRmStorageContainerLegalHold -StorageAccount $accountObject -ContainerName "myContainer"  -Tag  tag1
```

<span data-ttu-id="37c7f-114">To polecenie umożliwia dodanie znaczników w postaci prawnej do kontenera obiektu blob magazynu z obiektem konta magazynu i nazwą kontenera.</span><span class="sxs-lookup"><span data-stu-id="37c7f-114">This command adds legal hold tags to a Storage blob container with Storage account object and container name.</span></span>

### <span data-ttu-id="37c7f-115">Przykład 3: Dodawanie znaczników w postaci prawnej do wszystkich kontenerów obiektów blob magazynu na koncie magazynu z potokiem</span><span class="sxs-lookup"><span data-stu-id="37c7f-115">Example 3: Add legal hold tags to all Storage blob containers in a Storage account with pipeline</span></span>
```
PS C:\>Get-AzureRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" | Add-AzureRmStorageContainerLegalHold -Tag  tag1,tag2,tag3
```

<span data-ttu-id="37c7f-116">To polecenie umożliwia dodanie znaczników w postaci prawnej do wszystkich kontenerów obiektów blob magazynu na koncie magazynu z potokiem.</span><span class="sxs-lookup"><span data-stu-id="37c7f-116">This command adds legal hold tags to all Storage blob containers in a Storage account with pipeline.</span></span>

## <span data-ttu-id="37c7f-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="37c7f-117">PARAMETERS</span></span>

### <span data-ttu-id="37c7f-118">-Kontener</span><span class="sxs-lookup"><span data-stu-id="37c7f-118">-Container</span></span>
<span data-ttu-id="37c7f-119">Obiekt kontenera magazynu</span><span class="sxs-lookup"><span data-stu-id="37c7f-119">Storage container object</span></span>

```yaml
Type: PSContainer
Parameter Sets: ContainerObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="37c7f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37c7f-120">-DefaultProfile</span></span>
<span data-ttu-id="37c7f-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="37c7f-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37c7f-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="37c7f-122">-Name</span></span>
<span data-ttu-id="37c7f-123">Nazwa kontenera</span><span class="sxs-lookup"><span data-stu-id="37c7f-123">Container Name</span></span>

```yaml
Type: String
Parameter Sets: AccountName, AccountObject
Aliases: N, ContainerName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="37c7f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37c7f-124">-ResourceGroupName</span></span>
<span data-ttu-id="37c7f-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="37c7f-125">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: AccountName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37c7f-126">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="37c7f-126">-StorageAccount</span></span>
<span data-ttu-id="37c7f-127">Obiekt konta magazynu</span><span class="sxs-lookup"><span data-stu-id="37c7f-127">Storage account object</span></span>

```yaml
Type: PSStorageAccount
Parameter Sets: AccountObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="37c7f-128">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="37c7f-128">-StorageAccountName</span></span>
<span data-ttu-id="37c7f-129">Nazwa konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="37c7f-129">Storage Account Name.</span></span>

```yaml
Type: String
Parameter Sets: AccountName
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37c7f-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="37c7f-130">-Tag</span></span>
<span data-ttu-id="37c7f-131">Tagi LegalHold kontenera</span><span class="sxs-lookup"><span data-stu-id="37c7f-131">Container LegalHold Tags</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37c7f-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="37c7f-132">-Confirm</span></span>
<span data-ttu-id="37c7f-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="37c7f-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37c7f-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="37c7f-134">-WhatIf</span></span>
<span data-ttu-id="37c7f-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="37c7f-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="37c7f-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="37c7f-136">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37c7f-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37c7f-137">CommonParameters</span></span>
<span data-ttu-id="37c7f-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37c7f-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37c7f-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="37c7f-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37c7f-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="37c7f-140">INPUTS</span></span>

### <span data-ttu-id="37c7f-141">System. String</span><span class="sxs-lookup"><span data-stu-id="37c7f-141">System.String</span></span>

## <span data-ttu-id="37c7f-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="37c7f-142">OUTPUTS</span></span>

### <span data-ttu-id="37c7f-143">Microsoft. Azure. Commands. Management. Storage. models. PSLegalHold</span><span class="sxs-lookup"><span data-stu-id="37c7f-143">Microsoft.Azure.Commands.Management.Storage.Models.PSLegalHold</span></span>

## <span data-ttu-id="37c7f-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="37c7f-144">NOTES</span></span>

## <span data-ttu-id="37c7f-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="37c7f-145">RELATED LINKS</span></span>

