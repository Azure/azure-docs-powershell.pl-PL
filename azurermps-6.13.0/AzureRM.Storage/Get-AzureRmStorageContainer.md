---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/get-azurermstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageContainer.md
ms.openlocfilehash: 64e3857ddd9a9bb00b94e3e550c6be33722990a3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525958"
---
# <span data-ttu-id="1c83b-101">Get-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="1c83b-101">Get-AzureRmStorageContainer</span></span>

## <span data-ttu-id="1c83b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1c83b-102">SYNOPSIS</span></span>
<span data-ttu-id="1c83b-103">Pobiera lub Wyświetla kontenery blob magazynu.</span><span class="sxs-lookup"><span data-stu-id="1c83b-103">Gets or lists Storage blob containers</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1c83b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1c83b-104">SYNTAX</span></span>

### <span data-ttu-id="1c83b-105">AccountName (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="1c83b-105">AccountName (Default)</span></span>
```
Get-AzureRmStorageContainer [-ResourceGroupName] <String> [-StorageAccountName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1c83b-106">AccountName</span><span class="sxs-lookup"><span data-stu-id="1c83b-106">AccountObject</span></span>
```
Get-AzureRmStorageContainer -StorageAccount <PSStorageAccount> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1c83b-107">Opis</span><span class="sxs-lookup"><span data-stu-id="1c83b-107">DESCRIPTION</span></span>
<span data-ttu-id="1c83b-108">Polecenie cmdlet **Get-AzureRmStorageContainer** Pobiera lub Wyświetla kontenery blob magazynu.</span><span class="sxs-lookup"><span data-stu-id="1c83b-108">The **Get-AzureRmStorageContainer** cmdlet gets or lists  Storage blob containers</span></span>

## <span data-ttu-id="1c83b-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1c83b-109">EXAMPLES</span></span>

### <span data-ttu-id="1c83b-110">Przykład 1: Pobierz kontener obiektu blob magazynu z nazwą konta magazynu i nazwą kontenera</span><span class="sxs-lookup"><span data-stu-id="1c83b-110">Example 1: Get a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Get-AzureRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" 
```

<span data-ttu-id="1c83b-111">To polecenie pobiera kontener obiektu blob magazynu z nazwą konta magazynu i nazwą kontenera.</span><span class="sxs-lookup"><span data-stu-id="1c83b-111">This command gets a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="1c83b-112">Przykład 2: Lista wszystkich kontenerów obiektów blob magazynu dotyczących konta magazynu</span><span class="sxs-lookup"><span data-stu-id="1c83b-112">Example 2: List  all Storage blob containers of a Storage account</span></span>
```
PS C:\>Get-AzureRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" 
```

<span data-ttu-id="1c83b-113">To polecenie wyświetla listę wszystkich kontenerów obiektów blob magazynu z konta magazynu z nazwą konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="1c83b-113">This command lists all Storage blob containers of a Storage account with Storage account name.</span></span>

### <span data-ttu-id="1c83b-114">Przykład 3: Pobierz kontener obiektu blob magazynu z obiektem konta magazynu i nazwą kontenera.</span><span class="sxs-lookup"><span data-stu-id="1c83b-114">Example 3: Get a Storage blob container with Storage account object and container name.</span></span>
```
PS C:\>$accountObject = Get-AzureRmStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Get-AzureRmStorageContainer -StorageAccount $accountObject -ContainerName "myContainer" 
```

<span data-ttu-id="1c83b-115">To polecenie pobiera kontener obiektu blob magazynu z obiektem konta magazynu i nazwą kontenera.</span><span class="sxs-lookup"><span data-stu-id="1c83b-115">This command gets a Storage blob container with Storage account object and container name.</span></span>

## <span data-ttu-id="1c83b-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1c83b-116">PARAMETERS</span></span>

### <span data-ttu-id="1c83b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c83b-117">-DefaultProfile</span></span>
<span data-ttu-id="1c83b-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1c83b-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1c83b-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="1c83b-119">-Name</span></span>
<span data-ttu-id="1c83b-120">Nazwa kontenera</span><span class="sxs-lookup"><span data-stu-id="1c83b-120">Container Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, ContainerName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1c83b-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c83b-121">-ResourceGroupName</span></span>
<span data-ttu-id="1c83b-122">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="1c83b-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="1c83b-123">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="1c83b-123">-StorageAccount</span></span>
<span data-ttu-id="1c83b-124">Obiekt konta magazynu</span><span class="sxs-lookup"><span data-stu-id="1c83b-124">Storage account object</span></span>

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

### <span data-ttu-id="1c83b-125">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="1c83b-125">-StorageAccountName</span></span>
<span data-ttu-id="1c83b-126">Nazwa konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="1c83b-126">Storage Account Name.</span></span>

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

### <span data-ttu-id="1c83b-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c83b-127">CommonParameters</span></span>
<span data-ttu-id="1c83b-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c83b-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c83b-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1c83b-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c83b-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1c83b-130">INPUTS</span></span>

### <span data-ttu-id="1c83b-131">System. String</span><span class="sxs-lookup"><span data-stu-id="1c83b-131">System.String</span></span>

## <span data-ttu-id="1c83b-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1c83b-132">OUTPUTS</span></span>

### <span data-ttu-id="1c83b-133">Microsoft. Azure. Commands. Management. Storage. models. PSContainer</span><span class="sxs-lookup"><span data-stu-id="1c83b-133">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="1c83b-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1c83b-134">NOTES</span></span>

## <span data-ttu-id="1c83b-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1c83b-135">RELATED LINKS</span></span>

