---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azrmstoragecontainerimmutabilitypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzRmStorageContainerImmutabilityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzRmStorageContainerImmutabilityPolicy.md
ms.openlocfilehash: 2a1dee58ba741e5bd1c1122b704c5d62666338f2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94234238"
---
# <span data-ttu-id="f4d41-101">Get-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="f4d41-101">Get-AzRmStorageContainerImmutabilityPolicy</span></span>

## <span data-ttu-id="f4d41-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f4d41-102">SYNOPSIS</span></span>
<span data-ttu-id="f4d41-103">Pobiera ImmutabilityPolicy kontenerów blob magazynu.</span><span class="sxs-lookup"><span data-stu-id="f4d41-103">Gets ImmutabilityPolicy of a Storage blob containers</span></span>

## <span data-ttu-id="f4d41-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f4d41-104">SYNTAX</span></span>

### <span data-ttu-id="f4d41-105">AccountName (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="f4d41-105">AccountName (Default)</span></span>
```
Get-AzRmStorageContainerImmutabilityPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -ContainerName <String> [-Etag <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f4d41-106">AccountName</span><span class="sxs-lookup"><span data-stu-id="f4d41-106">AccountObject</span></span>
```
Get-AzRmStorageContainerImmutabilityPolicy -ContainerName <String> -StorageAccount <PSStorageAccount>
 [-Etag <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f4d41-107">Containerobject</span><span class="sxs-lookup"><span data-stu-id="f4d41-107">ContainerObject</span></span>
```
Get-AzRmStorageContainerImmutabilityPolicy -Container <PSContainer> [-Etag <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f4d41-108">Opis</span><span class="sxs-lookup"><span data-stu-id="f4d41-108">DESCRIPTION</span></span>
<span data-ttu-id="f4d41-109">Polecenie cmdlet **Get-AzRmStorageContainerImmutabilityPolicy** pobiera ImmutabilityPolicy kontenerów blob magazynu</span><span class="sxs-lookup"><span data-stu-id="f4d41-109">The **Get-AzRmStorageContainerImmutabilityPolicy** cmdlet gets ImmutabilityPolicy of a Storage blob containers</span></span>

## <span data-ttu-id="f4d41-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f4d41-110">EXAMPLES</span></span>

### <span data-ttu-id="f4d41-111">Przykład 1: pobieranie ImmutabilityPolicy kontenera obiektów blob magazynu z nazwą konta magazynu i nazwą kontenera</span><span class="sxs-lookup"><span data-stu-id="f4d41-111">Example 1: Get ImmutabilityPolicy of a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Get-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer"
```

<span data-ttu-id="f4d41-112">To polecenie pobiera ImmutabilityPolicy kontenera obiektów BLOB magazynowania z nazwą konta magazynu i nazwą kontenera.</span><span class="sxs-lookup"><span data-stu-id="f4d41-112">This command gets ImmutabilityPolicy of a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="f4d41-113">Przykład 2: pobieranie ImmutabilityPolicy kontenera obiektów BLOB magazynowania z obiektem konta magazynu i nazwą kontenera</span><span class="sxs-lookup"><span data-stu-id="f4d41-113">Example 2: Get ImmutabilityPolicy of a Storage blob container with Storage account object and container name</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Get-AzRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer"
```

<span data-ttu-id="f4d41-114">To polecenie pobiera ImmutabilityPolicy kontenerów blob magazynu z obiektem konta magazynu i nazwą kontenera.</span><span class="sxs-lookup"><span data-stu-id="f4d41-114">This command gets ImmutabilityPolicy of a Storage blob containers with Storage account object and container name.</span></span>

### <span data-ttu-id="f4d41-115">Przykład 3: pobieranie ImmutabilityPolicy kontenera obiektów BLOB magazynowania z obiektem kontenera magazynu</span><span class="sxs-lookup"><span data-stu-id="f4d41-115">Example 3: Get ImmutabilityPolicy of a Storage blob container with Storage container object</span></span>
```
PS C:\>$containerObject = Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -Name "myContainer"
PS C:\>Get-AzRmStorageContainerImmutabilityPolicy -Container $containerObject
```

<span data-ttu-id="f4d41-116">To polecenie pobiera ImmutabilityPolicy kontenera obiektów BLOB magazynowania z obiektem kontenera magazynu.</span><span class="sxs-lookup"><span data-stu-id="f4d41-116">This command gets ImmutabilityPolicy of a Storage blob container with Storage container object.</span></span>

## <span data-ttu-id="f4d41-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f4d41-117">PARAMETERS</span></span>

### <span data-ttu-id="f4d41-118">-Kontener</span><span class="sxs-lookup"><span data-stu-id="f4d41-118">-Container</span></span>
<span data-ttu-id="f4d41-119">Obiekt kontenera magazynu</span><span class="sxs-lookup"><span data-stu-id="f4d41-119">Storage container object</span></span>

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

### <span data-ttu-id="f4d41-120">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="f4d41-120">-ContainerName</span></span>
<span data-ttu-id="f4d41-121">Nazwa kontenera</span><span class="sxs-lookup"><span data-stu-id="f4d41-121">Container Name</span></span>

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

### <span data-ttu-id="f4d41-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4d41-122">-DefaultProfile</span></span>
<span data-ttu-id="f4d41-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f4d41-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f4d41-124">-ETag</span><span class="sxs-lookup"><span data-stu-id="f4d41-124">-Etag</span></span>
<span data-ttu-id="f4d41-125">Element ETag zasad Immutability.</span><span class="sxs-lookup"><span data-stu-id="f4d41-125">Immutability policy etag.</span></span>

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

### <span data-ttu-id="f4d41-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4d41-126">-ResourceGroupName</span></span>
<span data-ttu-id="f4d41-127">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f4d41-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="f4d41-128">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="f4d41-128">-StorageAccount</span></span>
<span data-ttu-id="f4d41-129">Obiekt konta magazynu</span><span class="sxs-lookup"><span data-stu-id="f4d41-129">Storage account object</span></span>

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

### <span data-ttu-id="f4d41-130">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="f4d41-130">-StorageAccountName</span></span>
<span data-ttu-id="f4d41-131">Nazwa konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="f4d41-131">Storage Account Name.</span></span>

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

### <span data-ttu-id="f4d41-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4d41-132">CommonParameters</span></span>
<span data-ttu-id="f4d41-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4d41-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4d41-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f4d41-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4d41-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f4d41-135">INPUTS</span></span>

### <span data-ttu-id="f4d41-136">System. String</span><span class="sxs-lookup"><span data-stu-id="f4d41-136">System.String</span></span>

### <span data-ttu-id="f4d41-137">Microsoft. Azure. Commands. Management. Storage. models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f4d41-137">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="f4d41-138">Microsoft. Azure. Commands. Management. Storage. models. PSContainer</span><span class="sxs-lookup"><span data-stu-id="f4d41-138">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="f4d41-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f4d41-139">OUTPUTS</span></span>

### <span data-ttu-id="f4d41-140">Microsoft. Azure. Commands. Management. Storage. models. PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="f4d41-140">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="f4d41-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f4d41-141">NOTES</span></span>

## <span data-ttu-id="f4d41-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f4d41-142">RELATED LINKS</span></span>
