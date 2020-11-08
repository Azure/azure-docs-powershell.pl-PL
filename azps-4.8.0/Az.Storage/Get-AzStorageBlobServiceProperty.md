---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageblobserviceproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlobServiceProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlobServiceProperty.md
ms.openlocfilehash: 7cdef2f35180712d0751149a85e4a422a868c389
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94061999"
---
# <span data-ttu-id="bb085-101">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="bb085-101">Get-AzStorageBlobServiceProperty</span></span>

## <span data-ttu-id="bb085-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bb085-102">SYNOPSIS</span></span>
<span data-ttu-id="bb085-103">Pobiera właściwości usługi dla usług blob magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="bb085-103">Gets service properties for Azure Storage Blob services.</span></span>

## <span data-ttu-id="bb085-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bb085-104">SYNTAX</span></span>

### <span data-ttu-id="bb085-105">AccountName (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="bb085-105">AccountName (Default)</span></span>
```
Get-AzStorageBlobServiceProperty [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bb085-106">AccountName</span><span class="sxs-lookup"><span data-stu-id="bb085-106">AccountObject</span></span>
```
Get-AzStorageBlobServiceProperty -StorageAccount <PSStorageAccount> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="bb085-107">BlobServicePropertiesResourceId</span><span class="sxs-lookup"><span data-stu-id="bb085-107">BlobServicePropertiesResourceId</span></span>
```
Get-AzStorageBlobServiceProperty [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bb085-108">Opis</span><span class="sxs-lookup"><span data-stu-id="bb085-108">DESCRIPTION</span></span>
<span data-ttu-id="bb085-109">Polecenie cmdlet **Get-AzStorageBlobServiceProperty** pobiera właściwości usługi dla usług BLOB usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="bb085-109">The **Get-AzStorageBlobServiceProperty** cmdlet gets the service properties for Azure Storage Blob services.</span></span>

## <span data-ttu-id="bb085-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bb085-110">EXAMPLES</span></span>

### <span data-ttu-id="bb085-111">Przykład 1: pobieranie właściwości usług blob magazynu platformy Azure określonego konta magazynu</span><span class="sxs-lookup"><span data-stu-id="bb085-111">Example 1: Get  Azure Storage Blob services property of a specified Storage Account</span></span>
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

<span data-ttu-id="bb085-112">To polecenie uzyskuje właściwość usługi BLOB dla określonego konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="bb085-112">This command gets the Blob services property of a specified Storage Account.</span></span>

## <span data-ttu-id="bb085-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bb085-113">PARAMETERS</span></span>

### <span data-ttu-id="bb085-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb085-114">-DefaultProfile</span></span>
<span data-ttu-id="bb085-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="bb085-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bb085-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb085-116">-ResourceGroupName</span></span>
<span data-ttu-id="bb085-117">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="bb085-117">Resource Group Name.</span></span>

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

### <span data-ttu-id="bb085-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bb085-118">-ResourceId</span></span>
<span data-ttu-id="bb085-119">Identyfikator zasobu właściwości usługi BLOB.</span><span class="sxs-lookup"><span data-stu-id="bb085-119">Blob Service Properties Resource Id.</span></span>

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

### <span data-ttu-id="bb085-120">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="bb085-120">-StorageAccount</span></span>
<span data-ttu-id="bb085-121">Obiekt konta magazynu</span><span class="sxs-lookup"><span data-stu-id="bb085-121">Storage account object</span></span>

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

### <span data-ttu-id="bb085-122">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="bb085-122">-StorageAccountName</span></span>
<span data-ttu-id="bb085-123">Nazwa konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="bb085-123">Storage Account Name.</span></span>

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

### <span data-ttu-id="bb085-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb085-124">CommonParameters</span></span>
<span data-ttu-id="bb085-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb085-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb085-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb085-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb085-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bb085-127">INPUTS</span></span>

### <span data-ttu-id="bb085-128">Microsoft. Azure. Commands. Management. Storage. models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="bb085-128">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="bb085-129">System. String</span><span class="sxs-lookup"><span data-stu-id="bb085-129">System.String</span></span>

## <span data-ttu-id="bb085-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bb085-130">OUTPUTS</span></span>

### <span data-ttu-id="bb085-131">Microsoft. Azure. Commands. Management. Storage. models. PSBlobServiceProperties</span><span class="sxs-lookup"><span data-stu-id="bb085-131">Microsoft.Azure.Commands.Management.Storage.Models.PSBlobServiceProperties</span></span>

## <span data-ttu-id="bb085-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bb085-132">NOTES</span></span>

## <span data-ttu-id="bb085-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bb085-133">RELATED LINKS</span></span>
