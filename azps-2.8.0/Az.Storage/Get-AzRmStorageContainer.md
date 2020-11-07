---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azrmstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzRmStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzRmStorageContainer.md
ms.openlocfilehash: aa2a03355431f027a9efd374f5af45199cc77452
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93887825"
---
# <span data-ttu-id="85124-101">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="85124-101">Get-AzRmStorageContainer</span></span>

## <span data-ttu-id="85124-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="85124-102">SYNOPSIS</span></span>
<span data-ttu-id="85124-103">Pobiera lub Wyświetla kontenery blob magazynu.</span><span class="sxs-lookup"><span data-stu-id="85124-103">Gets or lists Storage blob containers</span></span>

## <span data-ttu-id="85124-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="85124-104">SYNTAX</span></span>

### <span data-ttu-id="85124-105">AccountName (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="85124-105">AccountName (Default)</span></span>
```
Get-AzRmStorageContainer [-ResourceGroupName] <String> [-StorageAccountName] <String> [-Name <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="85124-106">AccountName</span><span class="sxs-lookup"><span data-stu-id="85124-106">AccountObject</span></span>
```
Get-AzRmStorageContainer -StorageAccount <PSStorageAccount> [-Name <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="85124-107">Opis</span><span class="sxs-lookup"><span data-stu-id="85124-107">DESCRIPTION</span></span>
<span data-ttu-id="85124-108">Polecenie cmdlet **Get-AzRmStorageContainer** Pobiera lub Wyświetla kontenery blob magazynu.</span><span class="sxs-lookup"><span data-stu-id="85124-108">The **Get-AzRmStorageContainer** cmdlet gets or lists  Storage blob containers</span></span>

## <span data-ttu-id="85124-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="85124-109">EXAMPLES</span></span>

### <span data-ttu-id="85124-110">Przykład 1: Pobierz kontener obiektu blob magazynu z nazwą konta magazynu i nazwą kontenera</span><span class="sxs-lookup"><span data-stu-id="85124-110">Example 1: Get a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Get-AzRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer"
```

<span data-ttu-id="85124-111">To polecenie pobiera kontener obiektu blob magazynu z nazwą konta magazynu i nazwą kontenera.</span><span class="sxs-lookup"><span data-stu-id="85124-111">This command gets a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="85124-112">Przykład 2: Lista wszystkich kontenerów obiektów blob magazynu dotyczących konta magazynu</span><span class="sxs-lookup"><span data-stu-id="85124-112">Example 2: List  all Storage blob containers of a Storage account</span></span>
```
PS C:\>Get-AzRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
```

<span data-ttu-id="85124-113">To polecenie wyświetla listę wszystkich kontenerów obiektów blob magazynu z konta magazynu z nazwą konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="85124-113">This command lists all Storage blob containers of a Storage account with Storage account name.</span></span>

### <span data-ttu-id="85124-114">Przykład 3: Pobierz kontener obiektu blob magazynu z obiektem konta magazynu i nazwą kontenera.</span><span class="sxs-lookup"><span data-stu-id="85124-114">Example 3: Get a Storage blob container with Storage account object and container name.</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Get-AzRmStorageContainer -StorageAccount $accountObject -ContainerName "myContainer"
```

<span data-ttu-id="85124-115">To polecenie pobiera kontener obiektu blob magazynu z obiektem konta magazynu i nazwą kontenera.</span><span class="sxs-lookup"><span data-stu-id="85124-115">This command gets a Storage blob container with Storage account object and container name.</span></span>

## <span data-ttu-id="85124-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="85124-116">PARAMETERS</span></span>

### <span data-ttu-id="85124-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="85124-117">-AsJob</span></span>
<span data-ttu-id="85124-118">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="85124-118">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85124-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85124-119">-DefaultProfile</span></span>
<span data-ttu-id="85124-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="85124-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="85124-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="85124-121">-Name</span></span>
<span data-ttu-id="85124-122">Nazwa kontenera</span><span class="sxs-lookup"><span data-stu-id="85124-122">Container Name</span></span>

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

### <span data-ttu-id="85124-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="85124-123">-ResourceGroupName</span></span>
<span data-ttu-id="85124-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="85124-124">Resource Group Name.</span></span>

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

### <span data-ttu-id="85124-125">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="85124-125">-StorageAccount</span></span>
<span data-ttu-id="85124-126">Obiekt konta magazynu</span><span class="sxs-lookup"><span data-stu-id="85124-126">Storage account object</span></span>

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

### <span data-ttu-id="85124-127">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="85124-127">-StorageAccountName</span></span>
<span data-ttu-id="85124-128">Nazwa konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="85124-128">Storage Account Name.</span></span>

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

### <span data-ttu-id="85124-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85124-129">CommonParameters</span></span>
<span data-ttu-id="85124-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85124-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85124-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="85124-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85124-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="85124-132">INPUTS</span></span>

### <span data-ttu-id="85124-133">System. String</span><span class="sxs-lookup"><span data-stu-id="85124-133">System.String</span></span>

### <span data-ttu-id="85124-134">Microsoft. Azure. Commands. Management. Storage. models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="85124-134">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="85124-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="85124-135">OUTPUTS</span></span>

### <span data-ttu-id="85124-136">Microsoft. Azure. Commands. Management. Storage. models. PSContainer</span><span class="sxs-lookup"><span data-stu-id="85124-136">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="85124-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="85124-137">NOTES</span></span>

## <span data-ttu-id="85124-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="85124-138">RELATED LINKS</span></span>
