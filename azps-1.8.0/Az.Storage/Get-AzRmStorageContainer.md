---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azrmstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzRmStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzRmStorageContainer.md
ms.openlocfilehash: f15d9905abbc7a61dc77d4e8b28c5942126d7b14
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93707658"
---
# <span data-ttu-id="d5b76-101">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="d5b76-101">Get-AzRmStorageContainer</span></span>

## <span data-ttu-id="d5b76-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d5b76-102">SYNOPSIS</span></span>
<span data-ttu-id="d5b76-103">Pobiera lub Wyświetla kontenery blob magazynu.</span><span class="sxs-lookup"><span data-stu-id="d5b76-103">Gets or lists Storage blob containers</span></span>

## <span data-ttu-id="d5b76-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d5b76-104">SYNTAX</span></span>

### <span data-ttu-id="d5b76-105">AccountName (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="d5b76-105">AccountName (Default)</span></span>
```
Get-AzRmStorageContainer [-ResourceGroupName] <String> [-StorageAccountName] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d5b76-106">AccountName</span><span class="sxs-lookup"><span data-stu-id="d5b76-106">AccountObject</span></span>
```
Get-AzRmStorageContainer -StorageAccount <PSStorageAccount> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d5b76-107">Opis</span><span class="sxs-lookup"><span data-stu-id="d5b76-107">DESCRIPTION</span></span>
<span data-ttu-id="d5b76-108">Polecenie cmdlet **Get-AzRmStorageContainer** Pobiera lub Wyświetla kontenery blob magazynu.</span><span class="sxs-lookup"><span data-stu-id="d5b76-108">The **Get-AzRmStorageContainer** cmdlet gets or lists  Storage blob containers</span></span>

## <span data-ttu-id="d5b76-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d5b76-109">EXAMPLES</span></span>

### <span data-ttu-id="d5b76-110">Przykład 1: Pobierz kontener obiektu blob magazynu z nazwą konta magazynu i nazwą kontenera</span><span class="sxs-lookup"><span data-stu-id="d5b76-110">Example 1: Get a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Get-AzRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer"
```

<span data-ttu-id="d5b76-111">To polecenie pobiera kontener obiektu blob magazynu z nazwą konta magazynu i nazwą kontenera.</span><span class="sxs-lookup"><span data-stu-id="d5b76-111">This command gets a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="d5b76-112">Przykład 2: Lista wszystkich kontenerów obiektów blob magazynu dotyczących konta magazynu</span><span class="sxs-lookup"><span data-stu-id="d5b76-112">Example 2: List  all Storage blob containers of a Storage account</span></span>
```
PS C:\>Get-AzRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
```

<span data-ttu-id="d5b76-113">To polecenie wyświetla listę wszystkich kontenerów obiektów blob magazynu z konta magazynu z nazwą konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="d5b76-113">This command lists all Storage blob containers of a Storage account with Storage account name.</span></span>

### <span data-ttu-id="d5b76-114">Przykład 3: Pobierz kontener obiektu blob magazynu z obiektem konta magazynu i nazwą kontenera.</span><span class="sxs-lookup"><span data-stu-id="d5b76-114">Example 3: Get a Storage blob container with Storage account object and container name.</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Get-AzRmStorageContainer -StorageAccount $accountObject -ContainerName "myContainer"
```

<span data-ttu-id="d5b76-115">To polecenie pobiera kontener obiektu blob magazynu z obiektem konta magazynu i nazwą kontenera.</span><span class="sxs-lookup"><span data-stu-id="d5b76-115">This command gets a Storage blob container with Storage account object and container name.</span></span>

## <span data-ttu-id="d5b76-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d5b76-116">PARAMETERS</span></span>

### <span data-ttu-id="d5b76-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5b76-117">-DefaultProfile</span></span>
<span data-ttu-id="d5b76-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d5b76-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d5b76-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d5b76-119">-Name</span></span>
<span data-ttu-id="d5b76-120">Nazwa kontenera</span><span class="sxs-lookup"><span data-stu-id="d5b76-120">Container Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, ContainerName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d5b76-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d5b76-121">-ResourceGroupName</span></span>
<span data-ttu-id="d5b76-122">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d5b76-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="d5b76-123">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="d5b76-123">-StorageAccount</span></span>
<span data-ttu-id="d5b76-124">Obiekt konta magazynu</span><span class="sxs-lookup"><span data-stu-id="d5b76-124">Storage account object</span></span>

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

### <span data-ttu-id="d5b76-125">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="d5b76-125">-StorageAccountName</span></span>
<span data-ttu-id="d5b76-126">Nazwa konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="d5b76-126">Storage Account Name.</span></span>

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

### <span data-ttu-id="d5b76-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5b76-127">CommonParameters</span></span>
<span data-ttu-id="d5b76-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d5b76-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5b76-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d5b76-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5b76-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d5b76-130">INPUTS</span></span>

### <span data-ttu-id="d5b76-131">System. String</span><span class="sxs-lookup"><span data-stu-id="d5b76-131">System.String</span></span>

### <span data-ttu-id="d5b76-132">Microsoft. Azure. Commands. Management. Storage. models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d5b76-132">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="d5b76-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d5b76-133">OUTPUTS</span></span>

### <span data-ttu-id="d5b76-134">Microsoft. Azure. Commands. Management. Storage. models. PSContainer</span><span class="sxs-lookup"><span data-stu-id="d5b76-134">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="d5b76-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d5b76-135">NOTES</span></span>

## <span data-ttu-id="d5b76-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d5b76-136">RELATED LINKS</span></span>
