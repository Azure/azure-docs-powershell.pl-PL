---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azrmstoragecontainerimmutabilitypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzRmStorageContainerImmutabilityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzRmStorageContainerImmutabilityPolicy.md
ms.openlocfilehash: 2a1dee58ba741e5bd1c1122b704c5d62666338f2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98376280"
---
# <span data-ttu-id="6178e-101">Get-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="6178e-101">Get-AzRmStorageContainerImmutabilityPolicy</span></span>

## <span data-ttu-id="6178e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6178e-102">SYNOPSIS</span></span>
<span data-ttu-id="6178e-103">Pobiera ImmutabilityPolicy kontenerów blob magazynu.</span><span class="sxs-lookup"><span data-stu-id="6178e-103">Gets ImmutabilityPolicy of a Storage blob containers</span></span>

## <span data-ttu-id="6178e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6178e-104">SYNTAX</span></span>

### <span data-ttu-id="6178e-105">AccountName (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="6178e-105">AccountName (Default)</span></span>
```
Get-AzRmStorageContainerImmutabilityPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -ContainerName <String> [-Etag <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6178e-106">AccountName</span><span class="sxs-lookup"><span data-stu-id="6178e-106">AccountObject</span></span>
```
Get-AzRmStorageContainerImmutabilityPolicy -ContainerName <String> -StorageAccount <PSStorageAccount>
 [-Etag <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6178e-107">Containerobject</span><span class="sxs-lookup"><span data-stu-id="6178e-107">ContainerObject</span></span>
```
Get-AzRmStorageContainerImmutabilityPolicy -Container <PSContainer> [-Etag <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6178e-108">Opis</span><span class="sxs-lookup"><span data-stu-id="6178e-108">DESCRIPTION</span></span>
<span data-ttu-id="6178e-109">Polecenie cmdlet **Get-AzRmStorageContainerImmutabilityPolicy** pobiera ImmutabilityPolicy kontenerów blob magazynu</span><span class="sxs-lookup"><span data-stu-id="6178e-109">The **Get-AzRmStorageContainerImmutabilityPolicy** cmdlet gets ImmutabilityPolicy of a Storage blob containers</span></span>

## <span data-ttu-id="6178e-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6178e-110">EXAMPLES</span></span>

### <span data-ttu-id="6178e-111">Przykład 1: pobieranie ImmutabilityPolicy kontenera obiektów blob magazynu z nazwą konta magazynu i nazwą kontenera</span><span class="sxs-lookup"><span data-stu-id="6178e-111">Example 1: Get ImmutabilityPolicy of a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Get-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer"
```

<span data-ttu-id="6178e-112">To polecenie pobiera ImmutabilityPolicy kontenera obiektów BLOB magazynowania z nazwą konta magazynu i nazwą kontenera.</span><span class="sxs-lookup"><span data-stu-id="6178e-112">This command gets ImmutabilityPolicy of a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="6178e-113">Przykład 2: pobieranie ImmutabilityPolicy kontenera obiektów BLOB magazynowania z obiektem konta magazynu i nazwą kontenera</span><span class="sxs-lookup"><span data-stu-id="6178e-113">Example 2: Get ImmutabilityPolicy of a Storage blob container with Storage account object and container name</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Get-AzRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer"
```

<span data-ttu-id="6178e-114">To polecenie pobiera ImmutabilityPolicy kontenerów blob magazynu z obiektem konta magazynu i nazwą kontenera.</span><span class="sxs-lookup"><span data-stu-id="6178e-114">This command gets ImmutabilityPolicy of a Storage blob containers with Storage account object and container name.</span></span>

### <span data-ttu-id="6178e-115">Przykład 3: pobieranie ImmutabilityPolicy kontenera obiektów BLOB magazynowania z obiektem kontenera magazynu</span><span class="sxs-lookup"><span data-stu-id="6178e-115">Example 3: Get ImmutabilityPolicy of a Storage blob container with Storage container object</span></span>
```
PS C:\>$containerObject = Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -Name "myContainer"
PS C:\>Get-AzRmStorageContainerImmutabilityPolicy -Container $containerObject
```

<span data-ttu-id="6178e-116">To polecenie pobiera ImmutabilityPolicy kontenera obiektów BLOB magazynowania z obiektem kontenera magazynu.</span><span class="sxs-lookup"><span data-stu-id="6178e-116">This command gets ImmutabilityPolicy of a Storage blob container with Storage container object.</span></span>

## <span data-ttu-id="6178e-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6178e-117">PARAMETERS</span></span>

### <span data-ttu-id="6178e-118">-Kontener</span><span class="sxs-lookup"><span data-stu-id="6178e-118">-Container</span></span>
<span data-ttu-id="6178e-119">Obiekt kontenera magazynu</span><span class="sxs-lookup"><span data-stu-id="6178e-119">Storage container object</span></span>

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

### <span data-ttu-id="6178e-120">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="6178e-120">-ContainerName</span></span>
<span data-ttu-id="6178e-121">Nazwa kontenera</span><span class="sxs-lookup"><span data-stu-id="6178e-121">Container Name</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountObject
Aliases: N

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6178e-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6178e-122">-DefaultProfile</span></span>
<span data-ttu-id="6178e-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6178e-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6178e-124">-ETag</span><span class="sxs-lookup"><span data-stu-id="6178e-124">-Etag</span></span>
<span data-ttu-id="6178e-125">Element ETag zasad Immutability.</span><span class="sxs-lookup"><span data-stu-id="6178e-125">Immutability policy etag.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IfMatch

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6178e-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6178e-126">-ResourceGroupName</span></span>
<span data-ttu-id="6178e-127">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="6178e-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="6178e-128">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="6178e-128">-StorageAccount</span></span>
<span data-ttu-id="6178e-129">Obiekt konta magazynu</span><span class="sxs-lookup"><span data-stu-id="6178e-129">Storage account object</span></span>

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

### <span data-ttu-id="6178e-130">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="6178e-130">-StorageAccountName</span></span>
<span data-ttu-id="6178e-131">Nazwa konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="6178e-131">Storage Account Name.</span></span>

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

### <span data-ttu-id="6178e-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6178e-132">CommonParameters</span></span>
<span data-ttu-id="6178e-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6178e-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6178e-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6178e-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6178e-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6178e-135">INPUTS</span></span>

### <span data-ttu-id="6178e-136">System. String</span><span class="sxs-lookup"><span data-stu-id="6178e-136">System.String</span></span>

### <span data-ttu-id="6178e-137">Microsoft. Azure. Commands. Management. Storage. models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6178e-137">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="6178e-138">Microsoft. Azure. Commands. Management. Storage. models. PSContainer</span><span class="sxs-lookup"><span data-stu-id="6178e-138">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="6178e-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6178e-139">OUTPUTS</span></span>

### <span data-ttu-id="6178e-140">Microsoft. Azure. Commands. Management. Storage. models. PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="6178e-140">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="6178e-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6178e-141">NOTES</span></span>

## <span data-ttu-id="6178e-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6178e-142">RELATED LINKS</span></span>
