---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: C2EBCCF0-56CE-4D49-A138-74E52FC3A9AC
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragequeue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageQueue.md
ms.openlocfilehash: 1f0e9f17ea6d240f9f29f677325173e0bbef38f9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93707619"
---
# <span data-ttu-id="68555-101">Get-AzStorageQueue</span><span class="sxs-lookup"><span data-stu-id="68555-101">Get-AzStorageQueue</span></span>

## <span data-ttu-id="68555-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="68555-102">SYNOPSIS</span></span>
<span data-ttu-id="68555-103">Zawiera listę kolejek przechowywania.</span><span class="sxs-lookup"><span data-stu-id="68555-103">Lists storage queues.</span></span>

## <span data-ttu-id="68555-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="68555-104">SYNTAX</span></span>

### <span data-ttu-id="68555-105">QueueName (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="68555-105">QueueName (Default)</span></span>
```
Get-AzStorageQueue [[-Name] <String>] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="68555-106">QueuePrefix</span><span class="sxs-lookup"><span data-stu-id="68555-106">QueuePrefix</span></span>
```
Get-AzStorageQueue -Prefix <String> [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="68555-107">Opis</span><span class="sxs-lookup"><span data-stu-id="68555-107">DESCRIPTION</span></span>
<span data-ttu-id="68555-108">Polecenie cmdlet **Get-AzStorageQueue** zawiera listę kolejek magazynowania skojarzonych z kontem usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="68555-108">The **Get-AzStorageQueue** cmdlet lists storage queues associated with an Azure Storage account.</span></span>

## <span data-ttu-id="68555-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="68555-109">EXAMPLES</span></span>

### <span data-ttu-id="68555-110">Przykład 1. Lista wszystkich kolejek w usłudze Azure Storage</span><span class="sxs-lookup"><span data-stu-id="68555-110">Example 1: List all Azure Storage queues</span></span>
```
PS C:\>Get-AzStorageQueue
```

<span data-ttu-id="68555-111">To polecenie powoduje wyświetlenie listy wszystkich kolejek magazynu dla bieżącego konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="68555-111">This command gets a list of all storage queues for the current Storage account.</span></span>

### <span data-ttu-id="68555-112">Przykład 2: Wyświetlanie listy kolejek magazynu platformy Azure przy użyciu znaku wieloznacznego</span><span class="sxs-lookup"><span data-stu-id="68555-112">Example 2: List Azure Storage queues using a wildcard character</span></span>
```
PS C:\>Get-AzStorageQueue -Name queue*
```

<span data-ttu-id="68555-113">To polecenie używa symbolu wieloznacznego w celu uzyskania listy kolejek przechowywania, których nazwy zaczynają się od kolejki.</span><span class="sxs-lookup"><span data-stu-id="68555-113">This command uses a wildcard character to get a list of storage queues whose name starts with queue.</span></span>

### <span data-ttu-id="68555-114">Przykład 3: Wyświetlanie listy kolejek magazynu platformy Azure przy użyciu prefiksu nazwy kolejki</span><span class="sxs-lookup"><span data-stu-id="68555-114">Example 3: List Azure Storage queues using queue name prefix</span></span>
```
PS C:\>Get-AzStorageQueue -Prefix "queue"
```

<span data-ttu-id="68555-115">W tym przykładzie użyto parametru *prefix* , aby uzyskać listę kolejek przechowywania, których nazwy zaczynają się od kolejki.</span><span class="sxs-lookup"><span data-stu-id="68555-115">This example uses the *Prefix* parameter to get a list of storage queues whose name starts with queue.</span></span>

## <span data-ttu-id="68555-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="68555-116">PARAMETERS</span></span>

### <span data-ttu-id="68555-117">-Context</span><span class="sxs-lookup"><span data-stu-id="68555-117">-Context</span></span>
<span data-ttu-id="68555-118">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="68555-118">Specifies the Azure storage context.</span></span>
<span data-ttu-id="68555-119">Możesz ją utworzyć przy użyciu polecenia cmdlet **New-AzStorageContext** .</span><span class="sxs-lookup"><span data-stu-id="68555-119">You can create it by using the **New-AzStorageContext** cmdlet.</span></span>

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

### <span data-ttu-id="68555-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68555-120">-DefaultProfile</span></span>
<span data-ttu-id="68555-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="68555-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="68555-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="68555-122">-Name</span></span>
<span data-ttu-id="68555-123">Określa nazwę.</span><span class="sxs-lookup"><span data-stu-id="68555-123">Specifies a name.</span></span>
<span data-ttu-id="68555-124">Jeśli nie podano nazwy, polecenie cmdlet powoduje wyświetlenie listy wszystkich kolejek.</span><span class="sxs-lookup"><span data-stu-id="68555-124">If no name is specified, the cmdlet gets a list of all the queues.</span></span>
<span data-ttu-id="68555-125">Jeśli jest określona pełna lub częściowa nazwa, polecenie cmdlet pobiera wszystkie kolejki zgodne ze wzorcem nazwy.</span><span class="sxs-lookup"><span data-stu-id="68555-125">If a full or partial name is specified, the cmdlet gets all queues that match the name pattern.</span></span>

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

### <span data-ttu-id="68555-126">-Prefix</span><span class="sxs-lookup"><span data-stu-id="68555-126">-Prefix</span></span>
<span data-ttu-id="68555-127">Określa prefiks, którego nazwy są używane w nazwach kolejek, które chcesz pobrać.</span><span class="sxs-lookup"><span data-stu-id="68555-127">Specifies a prefix used in the name of the queues you want to get.</span></span>

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

### <span data-ttu-id="68555-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68555-128">CommonParameters</span></span>
<span data-ttu-id="68555-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="68555-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68555-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="68555-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68555-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="68555-131">INPUTS</span></span>

### <span data-ttu-id="68555-132">System. String</span><span class="sxs-lookup"><span data-stu-id="68555-132">System.String</span></span>

### <span data-ttu-id="68555-133">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="68555-133">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="68555-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="68555-134">OUTPUTS</span></span>

### <span data-ttu-id="68555-135">Microsoft. platformy windowsazure. Commands. Common. Storage. ResourceModel. AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="68555-135">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageQueue</span></span>

## <span data-ttu-id="68555-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="68555-136">NOTES</span></span>

## <span data-ttu-id="68555-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="68555-137">RELATED LINKS</span></span>

[<span data-ttu-id="68555-138">Nowe — AzStorageQueue</span><span class="sxs-lookup"><span data-stu-id="68555-138">New-AzStorageQueue</span></span>](./New-AzStorageQueue.md)

[<span data-ttu-id="68555-139">Remove-AzStorageQueue</span><span class="sxs-lookup"><span data-stu-id="68555-139">Remove-AzStorageQueue</span></span>](./Remove-AzStorageQueue.md)

