---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/remove-azurermstoragecontainerlegalhold
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Remove-AzureRmStorageContainerLegalHold.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Remove-AzureRmStorageContainerLegalHold.md
ms.openlocfilehash: da0793e7eb10f7b83d785aea34866842abe9b887
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93547311"
---
# <span data-ttu-id="fc96d-101">Remove-AzureRmStorageContainerLegalHold</span><span class="sxs-lookup"><span data-stu-id="fc96d-101">Remove-AzureRmStorageContainerLegalHold</span></span>

## <span data-ttu-id="fc96d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fc96d-102">SYNOPSIS</span></span>
<span data-ttu-id="fc96d-103">Usuwa z kontenera obiektów blob magazynu prawnego Tagi</span><span class="sxs-lookup"><span data-stu-id="fc96d-103">Removes legal hold tags from a Storage blob container</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fc96d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fc96d-104">SYNTAX</span></span>

### <span data-ttu-id="fc96d-105">AccountName (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="fc96d-105">AccountName (Default)</span></span>
```
Remove-AzureRmStorageContainerLegalHold [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -Name <String> -Tag <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fc96d-106">AccountName</span><span class="sxs-lookup"><span data-stu-id="fc96d-106">AccountObject</span></span>
```
Remove-AzureRmStorageContainerLegalHold -Name <String> -StorageAccount <PSStorageAccount> -Tag <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fc96d-107">Containerobject</span><span class="sxs-lookup"><span data-stu-id="fc96d-107">ContainerObject</span></span>
```
Remove-AzureRmStorageContainerLegalHold -Container <PSContainer> -Tag <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fc96d-108">Opis</span><span class="sxs-lookup"><span data-stu-id="fc96d-108">DESCRIPTION</span></span>
<span data-ttu-id="fc96d-109">Polecenie cmdlet **Remove-AzureRmStorageContainerLegalHold** usuwa z kontenera obiektów blob magazynu prawnego Tagi</span><span class="sxs-lookup"><span data-stu-id="fc96d-109">The **Remove-AzureRmStorageContainerLegalHold** cmdlet removes legal hold tags from a Storage blob container</span></span>

## <span data-ttu-id="fc96d-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fc96d-110">EXAMPLES</span></span>

### <span data-ttu-id="fc96d-111">Przykład 1: usuwanie prawnych znaczników blokad z kontenera obiektu blob magazynu z nazwą konta magazynu i nazwą kontenera</span><span class="sxs-lookup"><span data-stu-id="fc96d-111">Example 1: Remove legal hold tags from a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Remove-AzureRmStorageContainerLegalHold -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -Tag  tag1
```

<span data-ttu-id="fc96d-112">To polecenie usuwa prawne znaczniki blokad z kontenera obiektu blob magazynu z nazwą konta magazynu i nazwą kontenera.</span><span class="sxs-lookup"><span data-stu-id="fc96d-112">This command removes legal hold tags from a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="fc96d-113">Przykład 2: usuwanie dozwolonych znaczników blokad z kontenera obiektu BLOB magazynowania z obiektem konta magazynu i nazwą kontenera</span><span class="sxs-lookup"><span data-stu-id="fc96d-113">Example 2: Remove legal hold tags from a Storage blob container with Storage account object and container name</span></span>
```
PS C:\>$accountObject = Get-AzureRmStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Remove-AzureRmStorageContainerLegalHold -StorageAccount $accountObject -ContainerName "myContainer"  -Tag  tag1,tag2 
```

<span data-ttu-id="fc96d-114">To polecenie usuwa prawne znaczniki blokad z kontenera obiektu blob magazynu z obiektem konta magazynu i nazwą kontenera.</span><span class="sxs-lookup"><span data-stu-id="fc96d-114">This command removes legal hold tags from a Storage blob container with Storage account object and container name.</span></span>

### <span data-ttu-id="fc96d-115">Przykład 3: usuwanie prawnych znaczników blokad ze wszystkich kontenerów obiektów blob magazynu na koncie magazynu z potokiem</span><span class="sxs-lookup"><span data-stu-id="fc96d-115">Example 3: Remove legal hold tags from all Storage blob containers in a Storage account with pipeline</span></span>
```
PS C:\>Get-AzureRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" | Remove-AzureRmStorageContainerLegalHold -Tag  tag1
```

<span data-ttu-id="fc96d-116">To polecenie usuwa prawne znaczniki blokad ze wszystkich kontenerów obiektów blob magazynu na koncie magazynu z potokiem.</span><span class="sxs-lookup"><span data-stu-id="fc96d-116">This command removes legal hold tags from all Storage blob containers in a Storage account with pipeline.</span></span>


## <span data-ttu-id="fc96d-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fc96d-117">PARAMETERS</span></span>

### <span data-ttu-id="fc96d-118">-Kontener</span><span class="sxs-lookup"><span data-stu-id="fc96d-118">-Container</span></span>
<span data-ttu-id="fc96d-119">Obiekt kontenera magazynu</span><span class="sxs-lookup"><span data-stu-id="fc96d-119">Storage container object</span></span>

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

### <span data-ttu-id="fc96d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc96d-120">-DefaultProfile</span></span>
<span data-ttu-id="fc96d-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="fc96d-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fc96d-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="fc96d-122">-Name</span></span>
<span data-ttu-id="fc96d-123">Nazwa kontenera</span><span class="sxs-lookup"><span data-stu-id="fc96d-123">Container Name</span></span>

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

### <span data-ttu-id="fc96d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc96d-124">-ResourceGroupName</span></span>
<span data-ttu-id="fc96d-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="fc96d-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="fc96d-126">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="fc96d-126">-StorageAccount</span></span>
<span data-ttu-id="fc96d-127">Obiekt konta magazynu</span><span class="sxs-lookup"><span data-stu-id="fc96d-127">Storage account object</span></span>

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

### <span data-ttu-id="fc96d-128">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="fc96d-128">-StorageAccountName</span></span>
<span data-ttu-id="fc96d-129">Nazwa konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="fc96d-129">Storage Account Name.</span></span>

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

### <span data-ttu-id="fc96d-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="fc96d-130">-Tag</span></span>
<span data-ttu-id="fc96d-131">Tagi LegalHold kontenera</span><span class="sxs-lookup"><span data-stu-id="fc96d-131">Container LegalHold Tags</span></span>

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

### <span data-ttu-id="fc96d-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="fc96d-132">-Confirm</span></span>
<span data-ttu-id="fc96d-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fc96d-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fc96d-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fc96d-134">-WhatIf</span></span>
<span data-ttu-id="fc96d-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fc96d-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fc96d-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="fc96d-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fc96d-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc96d-137">CommonParameters</span></span>
<span data-ttu-id="fc96d-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc96d-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc96d-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc96d-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc96d-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fc96d-140">INPUTS</span></span>

### <span data-ttu-id="fc96d-141">System. String</span><span class="sxs-lookup"><span data-stu-id="fc96d-141">System.String</span></span>

## <span data-ttu-id="fc96d-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fc96d-142">OUTPUTS</span></span>

### <span data-ttu-id="fc96d-143">Microsoft. Azure. Commands. Management. Storage. models. PSLegalHold</span><span class="sxs-lookup"><span data-stu-id="fc96d-143">Microsoft.Azure.Commands.Management.Storage.Models.PSLegalHold</span></span>

## <span data-ttu-id="fc96d-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fc96d-144">NOTES</span></span>

## <span data-ttu-id="fc96d-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fc96d-145">RELATED LINKS</span></span>

