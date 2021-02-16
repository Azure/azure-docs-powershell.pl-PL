---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azrmstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzRmStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzRmStorageContainer.md
ms.openlocfilehash: da0ccdc791318f0a315bea8d2464d8d0852aec8b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100178258"
---
# <span data-ttu-id="6e2c2-101">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="6e2c2-101">Get-AzRmStorageContainer</span></span>

## <span data-ttu-id="6e2c2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6e2c2-102">SYNOPSIS</span></span>
<span data-ttu-id="6e2c2-103">Pobiera lub wyświetla kontenery obiektów blob magazynu</span><span class="sxs-lookup"><span data-stu-id="6e2c2-103">Gets or lists Storage blob containers</span></span>

## <span data-ttu-id="6e2c2-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="6e2c2-104">SYNTAX</span></span>

### <span data-ttu-id="6e2c2-105">AccountName (Default)</span><span class="sxs-lookup"><span data-stu-id="6e2c2-105">AccountName (Default)</span></span>
```
Get-AzRmStorageContainer [-ResourceGroupName] <String> [-StorageAccountName] <String> [-Name <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6e2c2-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="6e2c2-106">AccountObject</span></span>
```
Get-AzRmStorageContainer -StorageAccount <PSStorageAccount> [-Name <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6e2c2-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="6e2c2-107">DESCRIPTION</span></span>
<span data-ttu-id="6e2c2-108">Polecenie **cmdlet Get-AzRmStorageContainer** pobiera lub wyświetla kontenery obiektów blob magazynu</span><span class="sxs-lookup"><span data-stu-id="6e2c2-108">The **Get-AzRmStorageContainer** cmdlet gets or lists  Storage blob containers</span></span>

## <span data-ttu-id="6e2c2-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="6e2c2-109">EXAMPLES</span></span>

### <span data-ttu-id="6e2c2-110">Przykład 1. Uzyskiwanie kontenera obiektów blob magazynu z nazwą konta magazynu i nazwą kontenera</span><span class="sxs-lookup"><span data-stu-id="6e2c2-110">Example 1: Get a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Get-AzRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer"
```

<span data-ttu-id="6e2c2-111">To polecenie pobiera kontener obiektów blob magazynu z nazwą konta magazynu i nazwą kontenera.</span><span class="sxs-lookup"><span data-stu-id="6e2c2-111">This command gets a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="6e2c2-112">Przykład 2. Lista wszystkich kontenerów obiektów blob magazynu konta magazynu</span><span class="sxs-lookup"><span data-stu-id="6e2c2-112">Example 2: List  all Storage blob containers of a Storage account</span></span>
```
PS C:\>Get-AzRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
```

<span data-ttu-id="6e2c2-113">To polecenie zawiera listę wszystkich kontenerów obiektów blob magazynu z konta magazynu z nazwą konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="6e2c2-113">This command lists all Storage blob containers of a Storage account with Storage account name.</span></span>

### <span data-ttu-id="6e2c2-114">Przykład 3. Pobierz kontener obiektów blob magazynu z obiektem konta magazynu i nazwą kontenera.</span><span class="sxs-lookup"><span data-stu-id="6e2c2-114">Example 3: Get a Storage blob container with Storage account object and container name.</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Get-AzRmStorageContainer -StorageAccount $accountObject -ContainerName "myContainer"
```

<span data-ttu-id="6e2c2-115">To polecenie pobiera kontener obiektów blob magazynu z obiektem konta magazynu i nazwą kontenera.</span><span class="sxs-lookup"><span data-stu-id="6e2c2-115">This command gets a Storage blob container with Storage account object and container name.</span></span>

## <span data-ttu-id="6e2c2-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6e2c2-116">PARAMETERS</span></span>

### <span data-ttu-id="6e2c2-117">— AsJob</span><span class="sxs-lookup"><span data-stu-id="6e2c2-117">-AsJob</span></span>
<span data-ttu-id="6e2c2-118">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="6e2c2-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6e2c2-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e2c2-119">-DefaultProfile</span></span>
<span data-ttu-id="6e2c2-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="6e2c2-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6e2c2-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="6e2c2-121">-Name</span></span>
<span data-ttu-id="6e2c2-122">Nazwa kontenera</span><span class="sxs-lookup"><span data-stu-id="6e2c2-122">Container Name</span></span>

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

### <span data-ttu-id="6e2c2-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6e2c2-123">-ResourceGroupName</span></span>
<span data-ttu-id="6e2c2-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="6e2c2-124">Resource Group Name.</span></span>

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

### <span data-ttu-id="6e2c2-125">— StorageAccount</span><span class="sxs-lookup"><span data-stu-id="6e2c2-125">-StorageAccount</span></span>
<span data-ttu-id="6e2c2-126">Obiekt konta magazynu</span><span class="sxs-lookup"><span data-stu-id="6e2c2-126">Storage account object</span></span>

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

### <span data-ttu-id="6e2c2-127">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="6e2c2-127">-StorageAccountName</span></span>
<span data-ttu-id="6e2c2-128">Nazwa konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="6e2c2-128">Storage Account Name.</span></span>

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

### <span data-ttu-id="6e2c2-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e2c2-129">CommonParameters</span></span>
<span data-ttu-id="6e2c2-130">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6e2c2-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e2c2-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6e2c2-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e2c2-132">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6e2c2-132">INPUTS</span></span>

### <span data-ttu-id="6e2c2-133">System.String</span><span class="sxs-lookup"><span data-stu-id="6e2c2-133">System.String</span></span>

### <span data-ttu-id="6e2c2-134">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6e2c2-134">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="6e2c2-135">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="6e2c2-135">OUTPUTS</span></span>

### <span data-ttu-id="6e2c2-136">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span><span class="sxs-lookup"><span data-stu-id="6e2c2-136">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="6e2c2-137">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="6e2c2-137">NOTES</span></span>

## <span data-ttu-id="6e2c2-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6e2c2-138">RELATED LINKS</span></span>
