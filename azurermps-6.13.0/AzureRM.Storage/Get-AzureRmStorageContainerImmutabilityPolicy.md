---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/get-azurermstoragecontainerimmutabilitypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageContainerImmutabilityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageContainerImmutabilityPolicy.md
ms.openlocfilehash: cff5f387b6729f51634ee0466b099e1df8314589
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93551972"
---
# <span data-ttu-id="84524-101">Get-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="84524-101">Get-AzureRmStorageContainerImmutabilityPolicy</span></span>

## <span data-ttu-id="84524-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="84524-102">SYNOPSIS</span></span>
<span data-ttu-id="84524-103">Pobiera ImmutabilityPolicy kontenerów blob magazynu.</span><span class="sxs-lookup"><span data-stu-id="84524-103">Gets ImmutabilityPolicy of a Storage blob containers</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="84524-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="84524-104">SYNTAX</span></span>

### <span data-ttu-id="84524-105">AccountName (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="84524-105">AccountName (Default)</span></span>
```
Get-AzureRmStorageContainerImmutabilityPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-ContainerName] <String> [-Etag <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="84524-106">AccountName</span><span class="sxs-lookup"><span data-stu-id="84524-106">AccountObject</span></span>
```
Get-AzureRmStorageContainerImmutabilityPolicy [-ContainerName] <String> -StorageAccount <PSStorageAccount>
 [-Etag <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="84524-107">Containerobject</span><span class="sxs-lookup"><span data-stu-id="84524-107">ContainerObject</span></span>
```
Get-AzureRmStorageContainerImmutabilityPolicy -Container <PSContainer> [-Etag <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="84524-108">Opis</span><span class="sxs-lookup"><span data-stu-id="84524-108">DESCRIPTION</span></span>
<span data-ttu-id="84524-109">Polecenie cmdlet **Get-AzureRmStorageContainerImmutabilityPolicy** pobiera ImmutabilityPolicy kontenerów blob magazynu</span><span class="sxs-lookup"><span data-stu-id="84524-109">The **Get-AzureRmStorageContainerImmutabilityPolicy** cmdlet gets ImmutabilityPolicy of a Storage blob containers</span></span>

## <span data-ttu-id="84524-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="84524-110">EXAMPLES</span></span>

### <span data-ttu-id="84524-111">Przykład 1: pobieranie ImmutabilityPolicy kontenera obiektów blob magazynu z nazwą konta magazynu i nazwą kontenera</span><span class="sxs-lookup"><span data-stu-id="84524-111">Example 1: Get ImmutabilityPolicy of a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Get-AzureRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer"
```

<span data-ttu-id="84524-112">To polecenie pobiera ImmutabilityPolicy kontenera obiektów BLOB magazynowania z nazwą konta magazynu i nazwą kontenera.</span><span class="sxs-lookup"><span data-stu-id="84524-112">This command gets ImmutabilityPolicy of a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="84524-113">Przykład 2: pobieranie ImmutabilityPolicy kontenera obiektów BLOB magazynowania z obiektem konta magazynu i nazwą kontenera</span><span class="sxs-lookup"><span data-stu-id="84524-113">Example 2: Get ImmutabilityPolicy of a Storage blob container with Storage account object and container name</span></span>
```
PS C:\>$accountObject = Get-AzureRmStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Get-AzureRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer"
```

<span data-ttu-id="84524-114">To polecenie pobiera ImmutabilityPolicy kontenerów blob magazynu z obiektem konta magazynu i nazwą kontenera.</span><span class="sxs-lookup"><span data-stu-id="84524-114">This command gets ImmutabilityPolicy of a Storage blob containers with Storage account object and container name.</span></span>

### <span data-ttu-id="84524-115">Przykład 3: pobieranie ImmutabilityPolicy kontenera obiektów BLOB magazynowania z obiektem kontenera magazynu</span><span class="sxs-lookup"><span data-stu-id="84524-115">Example 3: Get ImmutabilityPolicy of a Storage blob container with Storage container object</span></span>
```
PS C:\>$containerObject = Get-AzureRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -Name "myContainer"
PS C:\>Get-AzureRmStorageContainerImmutabilityPolicy -Container $containerObject 
```

<span data-ttu-id="84524-116">To polecenie pobiera ImmutabilityPolicy kontenera obiektów BLOB magazynowania z obiektem kontenera magazynu.</span><span class="sxs-lookup"><span data-stu-id="84524-116">This command gets ImmutabilityPolicy of a Storage blob container with Storage container object.</span></span>

## <span data-ttu-id="84524-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="84524-117">PARAMETERS</span></span>

### <span data-ttu-id="84524-118">-Kontener</span><span class="sxs-lookup"><span data-stu-id="84524-118">-Container</span></span>
<span data-ttu-id="84524-119">Obiekt kontenera magazynu</span><span class="sxs-lookup"><span data-stu-id="84524-119">Storage container object</span></span>

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

### <span data-ttu-id="84524-120">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="84524-120">-ContainerName</span></span>
<span data-ttu-id="84524-121">Nazwa kontenera</span><span class="sxs-lookup"><span data-stu-id="84524-121">Container Name</span></span>

```yaml
Type: String
Parameter Sets: AccountName, AccountObject
Aliases: N

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="84524-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84524-122">-DefaultProfile</span></span>
<span data-ttu-id="84524-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="84524-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="84524-124">-ETag</span><span class="sxs-lookup"><span data-stu-id="84524-124">-Etag</span></span>
<span data-ttu-id="84524-125">Element ETag zasad Immutability.</span><span class="sxs-lookup"><span data-stu-id="84524-125">Immutability policy etag.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: IfMatch

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84524-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84524-126">-ResourceGroupName</span></span>
<span data-ttu-id="84524-127">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="84524-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="84524-128">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="84524-128">-StorageAccount</span></span>
<span data-ttu-id="84524-129">Obiekt konta magazynu</span><span class="sxs-lookup"><span data-stu-id="84524-129">Storage account object</span></span>

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

### <span data-ttu-id="84524-130">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="84524-130">-StorageAccountName</span></span>
<span data-ttu-id="84524-131">Nazwa konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="84524-131">Storage Account Name.</span></span>

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

### <span data-ttu-id="84524-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84524-132">CommonParameters</span></span>
<span data-ttu-id="84524-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="84524-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84524-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="84524-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84524-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="84524-135">INPUTS</span></span>

### <span data-ttu-id="84524-136">System. String</span><span class="sxs-lookup"><span data-stu-id="84524-136">System.String</span></span>

## <span data-ttu-id="84524-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="84524-137">OUTPUTS</span></span>

### <span data-ttu-id="84524-138">Microsoft. Azure. Commands. Management. Storage. models. PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="84524-138">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="84524-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="84524-139">NOTES</span></span>

## <span data-ttu-id="84524-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="84524-140">RELATED LINKS</span></span>

