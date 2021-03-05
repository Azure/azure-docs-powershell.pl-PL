---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/get-azrmstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzRmStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzRmStorageContainer.md
ms.openlocfilehash: c4f5fe5fa703d2706d37cd0bebf9df79fd272f5b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102002906"
---
# <span data-ttu-id="a1ec9-101">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="a1ec9-101">Get-AzRmStorageContainer</span></span>

## <span data-ttu-id="a1ec9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a1ec9-102">SYNOPSIS</span></span>
<span data-ttu-id="a1ec9-103">Pobiera lub wyświetla kontenery obiektów blob magazynu</span><span class="sxs-lookup"><span data-stu-id="a1ec9-103">Gets or lists Storage blob containers</span></span>

## <span data-ttu-id="a1ec9-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a1ec9-104">SYNTAX</span></span>

### <span data-ttu-id="a1ec9-105">AccountName (Default)</span><span class="sxs-lookup"><span data-stu-id="a1ec9-105">AccountName (Default)</span></span>
```
Get-AzRmStorageContainer [-ResourceGroupName] <String> [-StorageAccountName] <String> [-Name <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a1ec9-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="a1ec9-106">AccountObject</span></span>
```
Get-AzRmStorageContainer -StorageAccount <PSStorageAccount> [-Name <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a1ec9-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="a1ec9-107">DESCRIPTION</span></span>
<span data-ttu-id="a1ec9-108">Polecenie **cmdlet Get-AzRmStorageContainer** pobiera lub wyświetla kontenery obiektów blob magazynu</span><span class="sxs-lookup"><span data-stu-id="a1ec9-108">The **Get-AzRmStorageContainer** cmdlet gets or lists  Storage blob containers</span></span>

## <span data-ttu-id="a1ec9-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a1ec9-109">EXAMPLES</span></span>

### <span data-ttu-id="a1ec9-110">Przykład 1. Uzyskiwanie kontenera obiektów blob magazynu z nazwą konta magazynu i nazwą kontenera</span><span class="sxs-lookup"><span data-stu-id="a1ec9-110">Example 1: Get a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Get-AzRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer"
```

<span data-ttu-id="a1ec9-111">To polecenie pobiera kontener obiektów blob magazynu z nazwą konta magazynu i nazwą kontenera.</span><span class="sxs-lookup"><span data-stu-id="a1ec9-111">This command gets a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="a1ec9-112">Przykład 2. Lista wszystkich kontenerów obiektów blob magazynu konta magazynu</span><span class="sxs-lookup"><span data-stu-id="a1ec9-112">Example 2: List  all Storage blob containers of a Storage account</span></span>
```
PS C:\>Get-AzRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
```

<span data-ttu-id="a1ec9-113">To polecenie zawiera listę wszystkich kontenerów obiektów blob magazynu na koncie magazynu z nazwą konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="a1ec9-113">This command lists all Storage blob containers of a Storage account with Storage account name.</span></span>

### <span data-ttu-id="a1ec9-114">Przykład 3. Pobierz kontener obiektów blob magazynu z obiektem konta magazynu i nazwą kontenera.</span><span class="sxs-lookup"><span data-stu-id="a1ec9-114">Example 3: Get a Storage blob container with Storage account object and container name.</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Get-AzRmStorageContainer -StorageAccount $accountObject -ContainerName "myContainer"
```

<span data-ttu-id="a1ec9-115">To polecenie pobiera kontener obiektów blob magazynu z obiektem konta magazynu i nazwą kontenera.</span><span class="sxs-lookup"><span data-stu-id="a1ec9-115">This command gets a Storage blob container with Storage account object and container name.</span></span>

## <span data-ttu-id="a1ec9-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a1ec9-116">PARAMETERS</span></span>

### <span data-ttu-id="a1ec9-117">— AsJob</span><span class="sxs-lookup"><span data-stu-id="a1ec9-117">-AsJob</span></span>
<span data-ttu-id="a1ec9-118">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="a1ec9-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a1ec9-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1ec9-119">-DefaultProfile</span></span>
<span data-ttu-id="a1ec9-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="a1ec9-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a1ec9-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="a1ec9-121">-Name</span></span>
<span data-ttu-id="a1ec9-122">Nazwa kontenera</span><span class="sxs-lookup"><span data-stu-id="a1ec9-122">Container Name</span></span>

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

### <span data-ttu-id="a1ec9-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1ec9-123">-ResourceGroupName</span></span>
<span data-ttu-id="a1ec9-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a1ec9-124">Resource Group Name.</span></span>

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

### <span data-ttu-id="a1ec9-125">— StorageAccount</span><span class="sxs-lookup"><span data-stu-id="a1ec9-125">-StorageAccount</span></span>
<span data-ttu-id="a1ec9-126">Obiekt konta magazynu</span><span class="sxs-lookup"><span data-stu-id="a1ec9-126">Storage account object</span></span>

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

### <span data-ttu-id="a1ec9-127">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="a1ec9-127">-StorageAccountName</span></span>
<span data-ttu-id="a1ec9-128">Nazwa konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="a1ec9-128">Storage Account Name.</span></span>

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

### <span data-ttu-id="a1ec9-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1ec9-129">CommonParameters</span></span>
<span data-ttu-id="a1ec9-130">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1ec9-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1ec9-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a1ec9-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1ec9-132">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a1ec9-132">INPUTS</span></span>

### <span data-ttu-id="a1ec9-133">System.String</span><span class="sxs-lookup"><span data-stu-id="a1ec9-133">System.String</span></span>

### <span data-ttu-id="a1ec9-134">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a1ec9-134">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="a1ec9-135">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a1ec9-135">OUTPUTS</span></span>

### <span data-ttu-id="a1ec9-136">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span><span class="sxs-lookup"><span data-stu-id="a1ec9-136">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="a1ec9-137">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a1ec9-137">NOTES</span></span>

## <span data-ttu-id="a1ec9-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a1ec9-138">RELATED LINKS</span></span>
