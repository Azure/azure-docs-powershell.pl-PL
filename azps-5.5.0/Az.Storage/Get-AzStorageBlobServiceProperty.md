---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageblobserviceproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlobServiceProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlobServiceProperty.md
ms.openlocfilehash: 7cdef2f35180712d0751149a85e4a422a868c389
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100195810"
---
# <span data-ttu-id="17194-101">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="17194-101">Get-AzStorageBlobServiceProperty</span></span>

## <span data-ttu-id="17194-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="17194-102">SYNOPSIS</span></span>
<span data-ttu-id="17194-103">Pobiera właściwości usługi dla usług obiektów blob magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="17194-103">Gets service properties for Azure Storage Blob services.</span></span>

## <span data-ttu-id="17194-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="17194-104">SYNTAX</span></span>

### <span data-ttu-id="17194-105">AccountName (Default)</span><span class="sxs-lookup"><span data-stu-id="17194-105">AccountName (Default)</span></span>
```
Get-AzStorageBlobServiceProperty [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="17194-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="17194-106">AccountObject</span></span>
```
Get-AzStorageBlobServiceProperty -StorageAccount <PSStorageAccount> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="17194-107">BlobServicePropertiesResourceId</span><span class="sxs-lookup"><span data-stu-id="17194-107">BlobServicePropertiesResourceId</span></span>
```
Get-AzStorageBlobServiceProperty [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="17194-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="17194-108">DESCRIPTION</span></span>
<span data-ttu-id="17194-109">Polecenie **cmdlet Get-AzStorageBlobServiceProperty** pobiera właściwości usługi dla usług obiektów blob magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="17194-109">The **Get-AzStorageBlobServiceProperty** cmdlet gets the service properties for Azure Storage Blob services.</span></span>

## <span data-ttu-id="17194-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="17194-110">EXAMPLES</span></span>

### <span data-ttu-id="17194-111">Przykład 1. Uzyskiwanie właściwości usług obiektów blob magazynu platformy Azure dla określonego konta magazynu</span><span class="sxs-lookup"><span data-stu-id="17194-111">Example 1: Get  Azure Storage Blob services property of a specified Storage Account</span></span>
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

<span data-ttu-id="17194-112">To polecenie pobiera właściwość usług obiektów blob określonego konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="17194-112">This command gets the Blob services property of a specified Storage Account.</span></span>

## <span data-ttu-id="17194-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="17194-113">PARAMETERS</span></span>

### <span data-ttu-id="17194-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17194-114">-DefaultProfile</span></span>
<span data-ttu-id="17194-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="17194-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="17194-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17194-116">-ResourceGroupName</span></span>
<span data-ttu-id="17194-117">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="17194-117">Resource Group Name.</span></span>

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

### <span data-ttu-id="17194-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="17194-118">-ResourceId</span></span>
<span data-ttu-id="17194-119">Identyfikator zasobu właściwości usługi obiektów blob.</span><span class="sxs-lookup"><span data-stu-id="17194-119">Blob Service Properties Resource Id.</span></span>

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

### <span data-ttu-id="17194-120">— StorageAccount</span><span class="sxs-lookup"><span data-stu-id="17194-120">-StorageAccount</span></span>
<span data-ttu-id="17194-121">Obiekt konta magazynu</span><span class="sxs-lookup"><span data-stu-id="17194-121">Storage account object</span></span>

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

### <span data-ttu-id="17194-122">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="17194-122">-StorageAccountName</span></span>
<span data-ttu-id="17194-123">Nazwa konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="17194-123">Storage Account Name.</span></span>

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

### <span data-ttu-id="17194-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17194-124">CommonParameters</span></span>
<span data-ttu-id="17194-125">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="17194-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17194-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="17194-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17194-127">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="17194-127">INPUTS</span></span>

### <span data-ttu-id="17194-128">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="17194-128">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="17194-129">System.String</span><span class="sxs-lookup"><span data-stu-id="17194-129">System.String</span></span>

## <span data-ttu-id="17194-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="17194-130">OUTPUTS</span></span>

### <span data-ttu-id="17194-131">Microsoft.Azure.Commands.Management.Storage.Models.PSBlobServiceProperties</span><span class="sxs-lookup"><span data-stu-id="17194-131">Microsoft.Azure.Commands.Management.Storage.Models.PSBlobServiceProperties</span></span>

## <span data-ttu-id="17194-132">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="17194-132">NOTES</span></span>

## <span data-ttu-id="17194-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="17194-133">RELATED LINKS</span></span>
