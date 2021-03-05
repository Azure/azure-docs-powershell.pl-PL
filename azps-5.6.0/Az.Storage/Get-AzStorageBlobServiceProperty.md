---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/get-azstorageblobserviceproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlobServiceProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlobServiceProperty.md
ms.openlocfilehash: 72e26a8fbb059db78fcdfa56721bed94e388ef55
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102002666"
---
# <span data-ttu-id="c6c1c-101">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="c6c1c-101">Get-AzStorageBlobServiceProperty</span></span>

## <span data-ttu-id="c6c1c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c6c1c-102">SYNOPSIS</span></span>
<span data-ttu-id="c6c1c-103">Pobiera właściwości usługi dla usług obiektów blob magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="c6c1c-103">Gets service properties for Azure Storage Blob services.</span></span>

## <span data-ttu-id="c6c1c-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="c6c1c-104">SYNTAX</span></span>

### <span data-ttu-id="c6c1c-105">AccountName (Default)</span><span class="sxs-lookup"><span data-stu-id="c6c1c-105">AccountName (Default)</span></span>
```
Get-AzStorageBlobServiceProperty [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c6c1c-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="c6c1c-106">AccountObject</span></span>
```
Get-AzStorageBlobServiceProperty -StorageAccount <PSStorageAccount> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c6c1c-107">BlobServicePropertiesResourceId</span><span class="sxs-lookup"><span data-stu-id="c6c1c-107">BlobServicePropertiesResourceId</span></span>
```
Get-AzStorageBlobServiceProperty [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c6c1c-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="c6c1c-108">DESCRIPTION</span></span>
<span data-ttu-id="c6c1c-109">Polecenie **cmdlet Get-AzStorageBlobServiceProperty** pobiera właściwości usługi dla usług obiektów blob magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="c6c1c-109">The **Get-AzStorageBlobServiceProperty** cmdlet gets the service properties for Azure Storage Blob services.</span></span>

## <span data-ttu-id="c6c1c-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="c6c1c-110">EXAMPLES</span></span>

### <span data-ttu-id="c6c1c-111">Przykład 1. Pobierz właściwość usług blob magazynu platformy Azure dla określonego konta magazynu</span><span class="sxs-lookup"><span data-stu-id="c6c1c-111">Example 1: Get  Azure Storage Blob services property of a specified Storage Account</span></span>
```powershell
PS C:\> Get-AzStorageBlobServiceProperty -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount"

StorageAccountName            : mystorageaccount
ResourceGroupName             : myresourcegroup
DefaultServiceVersion         : 
DeleteRetentionPolicy.Enabled : False
DeleteRetentionPolicy.Days    : 
RestorePolicy.Enabled         : 
RestorePolicy.Days            : 
ChangeFeed                    : True
IsVersioningEnabled           : True
```

<span data-ttu-id="c6c1c-112">To polecenie pobiera właściwość usług obiektów blob określonego konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="c6c1c-112">This command gets the Blob services property of a specified Storage Account.</span></span>

## <span data-ttu-id="c6c1c-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c6c1c-113">PARAMETERS</span></span>

### <span data-ttu-id="c6c1c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6c1c-114">-DefaultProfile</span></span>
<span data-ttu-id="c6c1c-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="c6c1c-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c6c1c-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c6c1c-116">-ResourceGroupName</span></span>
<span data-ttu-id="c6c1c-117">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="c6c1c-117">Resource Group Name.</span></span>

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

### <span data-ttu-id="c6c1c-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c6c1c-118">-ResourceId</span></span>
<span data-ttu-id="c6c1c-119">Identyfikator zasobu właściwości usługi obiektów blob.</span><span class="sxs-lookup"><span data-stu-id="c6c1c-119">Blob Service Properties Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: BlobServicePropertiesResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6c1c-120">— StorageAccount</span><span class="sxs-lookup"><span data-stu-id="c6c1c-120">-StorageAccount</span></span>
<span data-ttu-id="c6c1c-121">Obiekt konta magazynu</span><span class="sxs-lookup"><span data-stu-id="c6c1c-121">Storage account object</span></span>

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

### <span data-ttu-id="c6c1c-122">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="c6c1c-122">-StorageAccountName</span></span>
<span data-ttu-id="c6c1c-123">Nazwa konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="c6c1c-123">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: AccountName, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6c1c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6c1c-124">CommonParameters</span></span>
<span data-ttu-id="c6c1c-125">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c6c1c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6c1c-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c6c1c-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6c1c-127">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c6c1c-127">INPUTS</span></span>

### <span data-ttu-id="c6c1c-128">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c6c1c-128">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="c6c1c-129">System.String</span><span class="sxs-lookup"><span data-stu-id="c6c1c-129">System.String</span></span>

## <span data-ttu-id="c6c1c-130">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c6c1c-130">OUTPUTS</span></span>

### <span data-ttu-id="c6c1c-131">Microsoft.Azure.Commands.Management.Storage.Models.PSBlobServiceProperties</span><span class="sxs-lookup"><span data-stu-id="c6c1c-131">Microsoft.Azure.Commands.Management.Storage.Models.PSBlobServiceProperties</span></span>

## <span data-ttu-id="c6c1c-132">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="c6c1c-132">NOTES</span></span>

## <span data-ttu-id="c6c1c-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c6c1c-133">RELATED LINKS</span></span>
