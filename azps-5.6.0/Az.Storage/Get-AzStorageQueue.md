---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: C2EBCCF0-56CE-4D49-A138-74E52FC3A9AC
online version: https://docs.microsoft.com/powershell/module/az.storage/get-azstoragequeue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageQueue.md
ms.openlocfilehash: 2361196f2e8b904f2403aaf06118122931e83afd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101997081"
---
# <span data-ttu-id="b915a-101">Get-AzStorageQueue</span><span class="sxs-lookup"><span data-stu-id="b915a-101">Get-AzStorageQueue</span></span>

## <span data-ttu-id="b915a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b915a-102">SYNOPSIS</span></span>
<span data-ttu-id="b915a-103">Lista kolejek magazynu.</span><span class="sxs-lookup"><span data-stu-id="b915a-103">Lists storage queues.</span></span>

## <span data-ttu-id="b915a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b915a-104">SYNTAX</span></span>

### <span data-ttu-id="b915a-105">QueueName (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="b915a-105">QueueName (Default)</span></span>
```
Get-AzStorageQueue [[-Name] <String>] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b915a-106">QueuePrefix</span><span class="sxs-lookup"><span data-stu-id="b915a-106">QueuePrefix</span></span>
```
Get-AzStorageQueue -Prefix <String> [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b915a-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="b915a-107">DESCRIPTION</span></span>
<span data-ttu-id="b915a-108">Polecenie **cmdlet Get-AzStorageQueue** wyświetla kolejki magazynu skojarzone z kontem usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="b915a-108">The **Get-AzStorageQueue** cmdlet lists storage queues associated with an Azure Storage account.</span></span>

## <span data-ttu-id="b915a-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b915a-109">EXAMPLES</span></span>

### <span data-ttu-id="b915a-110">Przykład 1. Lista wszystkich kolejek magazynu platformy Azure</span><span class="sxs-lookup"><span data-stu-id="b915a-110">Example 1: List all Azure Storage queues</span></span>
```
PS C:\>Get-AzStorageQueue
```

<span data-ttu-id="b915a-111">To polecenie otrzymuje listę wszystkich kolejek magazynu dla bieżącego konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="b915a-111">This command gets a list of all storage queues for the current Storage account.</span></span>

### <span data-ttu-id="b915a-112">Przykład 2. Lista kolejek magazynu platformy Azure przy użyciu symbolu wieloznacznego</span><span class="sxs-lookup"><span data-stu-id="b915a-112">Example 2: List Azure Storage queues using a wildcard character</span></span>
```
PS C:\>Get-AzStorageQueue -Name queue*
```

<span data-ttu-id="b915a-113">To polecenie używa symbolu wieloznacznego w celu uzyskania listy kolejek magazynu, których nazwa rozpoczyna się od kolejki.</span><span class="sxs-lookup"><span data-stu-id="b915a-113">This command uses a wildcard character to get a list of storage queues whose name starts with queue.</span></span>

### <span data-ttu-id="b915a-114">Przykład 3. Lista kolejek magazynu platformy Azure przy użyciu prefiksu nazwy kolejki</span><span class="sxs-lookup"><span data-stu-id="b915a-114">Example 3: List Azure Storage queues using queue name prefix</span></span>
```
PS C:\>Get-AzStorageQueue -Prefix "queue"
```

<span data-ttu-id="b915a-115">W tym przykładzie użyto *parametru Prefiks* w celu uzyskania listy kolejek magazynu, których nazwa zaczyna się od kolejki.</span><span class="sxs-lookup"><span data-stu-id="b915a-115">This example uses the *Prefix* parameter to get a list of storage queues whose name starts with queue.</span></span>

## <span data-ttu-id="b915a-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b915a-116">PARAMETERS</span></span>

### <span data-ttu-id="b915a-117">— kontekst</span><span class="sxs-lookup"><span data-stu-id="b915a-117">-Context</span></span>
<span data-ttu-id="b915a-118">Określa kontekst magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="b915a-118">Specifies the Azure storage context.</span></span>
<span data-ttu-id="b915a-119">Możesz go utworzyć za pomocą polecenia cmdlet **New-AzStorageContext.**</span><span class="sxs-lookup"><span data-stu-id="b915a-119">You can create it by using the **New-AzStorageContext** cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b915a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b915a-120">-DefaultProfile</span></span>
<span data-ttu-id="b915a-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="b915a-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b915a-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="b915a-122">-Name</span></span>
<span data-ttu-id="b915a-123">Określa nazwę.</span><span class="sxs-lookup"><span data-stu-id="b915a-123">Specifies a name.</span></span>
<span data-ttu-id="b915a-124">Jeśli nie zostanie określona żadna nazwa, polecenie cmdlet pobiera listę wszystkich kolejek.</span><span class="sxs-lookup"><span data-stu-id="b915a-124">If no name is specified, the cmdlet gets a list of all the queues.</span></span>
<span data-ttu-id="b915a-125">Jeśli zostanie określona pełna lub częściowa nazwa, polecenie cmdlet pobiera wszystkie kolejki zgodne ze wzorcem nazwy.</span><span class="sxs-lookup"><span data-stu-id="b915a-125">If a full or partial name is specified, the cmdlet gets all queues that match the name pattern.</span></span>

```yaml
Type: System.String
Parameter Sets: QueueName
Aliases: N, Queue

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b915a-126">—Prefiks</span><span class="sxs-lookup"><span data-stu-id="b915a-126">-Prefix</span></span>
<span data-ttu-id="b915a-127">Określa prefiks używany w nazwie kolejek, które mają zostać naniesiene.</span><span class="sxs-lookup"><span data-stu-id="b915a-127">Specifies a prefix used in the name of the queues you want to get.</span></span>

```yaml
Type: System.String
Parameter Sets: QueuePrefix
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b915a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b915a-128">CommonParameters</span></span>
<span data-ttu-id="b915a-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b915a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b915a-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b915a-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b915a-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b915a-131">INPUTS</span></span>

### <span data-ttu-id="b915a-132">System.String</span><span class="sxs-lookup"><span data-stu-id="b915a-132">System.String</span></span>

### <span data-ttu-id="b915a-133">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="b915a-133">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="b915a-134">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b915a-134">OUTPUTS</span></span>

### <span data-ttu-id="b915a-135">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="b915a-135">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageQueue</span></span>

## <span data-ttu-id="b915a-136">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b915a-136">NOTES</span></span>

## <span data-ttu-id="b915a-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b915a-137">RELATED LINKS</span></span>

[<span data-ttu-id="b915a-138">New-AzStorageQueue</span><span class="sxs-lookup"><span data-stu-id="b915a-138">New-AzStorageQueue</span></span>](./New-AzStorageQueue.md)

[<span data-ttu-id="b915a-139">Remove-AzStorageQueue</span><span class="sxs-lookup"><span data-stu-id="b915a-139">Remove-AzStorageQueue</span></span>](./Remove-AzStorageQueue.md)


