---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/get-azrmstoragecontainerimmutabilitypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzRmStorageContainerImmutabilityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzRmStorageContainerImmutabilityPolicy.md
ms.openlocfilehash: c1e68d77df44688961f867d473a9dfce1205c2dd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102002865"
---
# <span data-ttu-id="b62fe-101">Get-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="b62fe-101">Get-AzRmStorageContainerImmutabilityPolicy</span></span>

## <span data-ttu-id="b62fe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b62fe-102">SYNOPSIS</span></span>
<span data-ttu-id="b62fe-103">Pobiera politykę imutacji kontenerów obiektów blob magazynu</span><span class="sxs-lookup"><span data-stu-id="b62fe-103">Gets ImmutabilityPolicy of a Storage blob containers</span></span>

## <span data-ttu-id="b62fe-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b62fe-104">SYNTAX</span></span>

### <span data-ttu-id="b62fe-105">AccountName (Default)</span><span class="sxs-lookup"><span data-stu-id="b62fe-105">AccountName (Default)</span></span>
```
Get-AzRmStorageContainerImmutabilityPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -ContainerName <String> [-Etag <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b62fe-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="b62fe-106">AccountObject</span></span>
```
Get-AzRmStorageContainerImmutabilityPolicy -ContainerName <String> -StorageAccount <PSStorageAccount>
 [-Etag <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b62fe-107">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="b62fe-107">ContainerObject</span></span>
```
Get-AzRmStorageContainerImmutabilityPolicy -Container <PSContainer> [-Etag <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b62fe-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="b62fe-108">DESCRIPTION</span></span>
<span data-ttu-id="b62fe-109">Polecenie **cmdlet Get-AzRmStorageContainerImmutabilityPolicy** pobiera politykę ImmutabilityPolicy z kontenerów obiektów blob magazynu</span><span class="sxs-lookup"><span data-stu-id="b62fe-109">The **Get-AzRmStorageContainerImmutabilityPolicy** cmdlet gets ImmutabilityPolicy of a Storage blob containers</span></span>

## <span data-ttu-id="b62fe-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b62fe-110">EXAMPLES</span></span>

### <span data-ttu-id="b62fe-111">Przykład 1. Pobierz politykę immutability dla kontenera obiektów blob magazynu z nazwą konta magazynu i nazwą kontenera</span><span class="sxs-lookup"><span data-stu-id="b62fe-111">Example 1: Get ImmutabilityPolicy of a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Get-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer"
```

<span data-ttu-id="b62fe-112">To polecenie pobiera politykę immutability dla kontenera obiektów blob magazynu z nazwą konta magazynu i nazwą kontenera.</span><span class="sxs-lookup"><span data-stu-id="b62fe-112">This command gets ImmutabilityPolicy of a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="b62fe-113">Przykład 2. Uzyskiwanie właściwości ImmutabilityPolicy kontenera obiektów blob magazynu z obiektem konta magazynu i nazwą kontenera</span><span class="sxs-lookup"><span data-stu-id="b62fe-113">Example 2: Get ImmutabilityPolicy of a Storage blob container with Storage account object and container name</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Get-AzRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer"
```

<span data-ttu-id="b62fe-114">To polecenie pobiera politykę immutability dla kontenerów obiektów blob magazynu z obiektem konta magazynu i nazwą kontenera.</span><span class="sxs-lookup"><span data-stu-id="b62fe-114">This command gets ImmutabilityPolicy of a Storage blob containers with Storage account object and container name.</span></span>

### <span data-ttu-id="b62fe-115">Przykład 3. Uzyskiwanie właściwości ImmutabilityPolicy kontenera obiektów blob magazynu z obiektem kontenera magazynu</span><span class="sxs-lookup"><span data-stu-id="b62fe-115">Example 3: Get ImmutabilityPolicy of a Storage blob container with Storage container object</span></span>
```
PS C:\>$containerObject = Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -Name "myContainer"
PS C:\>Get-AzRmStorageContainerImmutabilityPolicy -Container $containerObject
```

<span data-ttu-id="b62fe-116">To polecenie pobiera politykę immutability dla kontenera obiektów blob magazynu z obiektem kontenera magazynu.</span><span class="sxs-lookup"><span data-stu-id="b62fe-116">This command gets ImmutabilityPolicy of a Storage blob container with Storage container object.</span></span>

## <span data-ttu-id="b62fe-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b62fe-117">PARAMETERS</span></span>

### <span data-ttu-id="b62fe-118">— Kontener</span><span class="sxs-lookup"><span data-stu-id="b62fe-118">-Container</span></span>
<span data-ttu-id="b62fe-119">Obiekt kontener magazynu</span><span class="sxs-lookup"><span data-stu-id="b62fe-119">Storage container object</span></span>

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

### <span data-ttu-id="b62fe-120">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="b62fe-120">-ContainerName</span></span>
<span data-ttu-id="b62fe-121">Nazwa kontenera</span><span class="sxs-lookup"><span data-stu-id="b62fe-121">Container Name</span></span>

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

### <span data-ttu-id="b62fe-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b62fe-122">-DefaultProfile</span></span>
<span data-ttu-id="b62fe-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="b62fe-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b62fe-124">— Otagowanie</span><span class="sxs-lookup"><span data-stu-id="b62fe-124">-Etag</span></span>
<span data-ttu-id="b62fe-125">Tag etag zasad wiadomości błyskawicznych.</span><span class="sxs-lookup"><span data-stu-id="b62fe-125">Immutability policy etag.</span></span>

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

### <span data-ttu-id="b62fe-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b62fe-126">-ResourceGroupName</span></span>
<span data-ttu-id="b62fe-127">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b62fe-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="b62fe-128">— StorageAccount</span><span class="sxs-lookup"><span data-stu-id="b62fe-128">-StorageAccount</span></span>
<span data-ttu-id="b62fe-129">Obiekt konta magazynu</span><span class="sxs-lookup"><span data-stu-id="b62fe-129">Storage account object</span></span>

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

### <span data-ttu-id="b62fe-130">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="b62fe-130">-StorageAccountName</span></span>
<span data-ttu-id="b62fe-131">Nazwa konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="b62fe-131">Storage Account Name.</span></span>

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

### <span data-ttu-id="b62fe-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b62fe-132">CommonParameters</span></span>
<span data-ttu-id="b62fe-133">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b62fe-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b62fe-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b62fe-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b62fe-135">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b62fe-135">INPUTS</span></span>

### <span data-ttu-id="b62fe-136">System.String</span><span class="sxs-lookup"><span data-stu-id="b62fe-136">System.String</span></span>

### <span data-ttu-id="b62fe-137">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b62fe-137">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="b62fe-138">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span><span class="sxs-lookup"><span data-stu-id="b62fe-138">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="b62fe-139">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b62fe-139">OUTPUTS</span></span>

### <span data-ttu-id="b62fe-140">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="b62fe-140">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="b62fe-141">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b62fe-141">NOTES</span></span>

## <span data-ttu-id="b62fe-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b62fe-142">RELATED LINKS</span></span>
