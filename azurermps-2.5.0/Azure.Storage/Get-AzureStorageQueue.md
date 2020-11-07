---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: C2EBCCF0-56CE-4D49-A138-74E52FC3A9AC
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestoragequeue
schema: 2.0.0
ms.openlocfilehash: 59a035a7af56a333a1ef91b5ce4aa2d1afbe5086
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93899417"
---
# <span data-ttu-id="93f46-101">Get-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="93f46-101">Get-AzureStorageQueue</span></span>

## <span data-ttu-id="93f46-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="93f46-102">SYNOPSIS</span></span>
<span data-ttu-id="93f46-103">Zawiera listę kolejek przechowywania.</span><span class="sxs-lookup"><span data-stu-id="93f46-103">Lists storage queues.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="93f46-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="93f46-104">SYNTAX</span></span>

### <span data-ttu-id="93f46-105">QueueName (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="93f46-105">QueueName (Default)</span></span>
```
Get-AzureStorageQueue [[-Name] <String>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="93f46-106">QueuePrefix</span><span class="sxs-lookup"><span data-stu-id="93f46-106">QueuePrefix</span></span>
```
Get-AzureStorageQueue -Prefix <String> [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="93f46-107">Opis</span><span class="sxs-lookup"><span data-stu-id="93f46-107">DESCRIPTION</span></span>
<span data-ttu-id="93f46-108">Polecenie cmdlet **Get-AzureStorageQueue** zawiera listę kolejek magazynowania skojarzonych z kontem usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="93f46-108">The **Get-AzureStorageQueue** cmdlet lists storage queues associated with an Azure Storage account.</span></span>

## <span data-ttu-id="93f46-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="93f46-109">EXAMPLES</span></span>

### <span data-ttu-id="93f46-110">Przykład 1. Lista wszystkich kolejek w usłudze Azure Storage</span><span class="sxs-lookup"><span data-stu-id="93f46-110">Example 1: List all Azure Storage queues</span></span>
```
PS C:\>Get-AzureStorageQueue
```

<span data-ttu-id="93f46-111">To polecenie powoduje wyświetlenie listy wszystkich kolejek magazynu dla bieżącego konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="93f46-111">This command gets a list of all storage queues for the current Storage account.</span></span>

### <span data-ttu-id="93f46-112">Przykład 2: Wyświetlanie listy kolejek magazynu platformy Azure przy użyciu znaku wieloznacznego</span><span class="sxs-lookup"><span data-stu-id="93f46-112">Example 2: List Azure Storage queues using a wildcard character</span></span>
```
PS C:\>Get-AzureStorageQueue -Name queue*
```

<span data-ttu-id="93f46-113">To polecenie używa symbolu wieloznacznego w celu uzyskania listy kolejek przechowywania, których nazwy zaczynają się od kolejki.</span><span class="sxs-lookup"><span data-stu-id="93f46-113">This command uses a wildcard character to get a list of storage queues whose name starts with queue.</span></span>

### <span data-ttu-id="93f46-114">Przykład 3: Wyświetlanie listy kolejek magazynu platformy Azure przy użyciu prefiksu nazwy kolejki</span><span class="sxs-lookup"><span data-stu-id="93f46-114">Example 3: List Azure Storage queues using queue name prefix</span></span>
```
PS C:\>Get-AzureStorageQueue -Prefix "queue"
```

<span data-ttu-id="93f46-115">W tym przykładzie użyto parametru *prefix* , aby uzyskać listę kolejek przechowywania, których nazwy zaczynają się od kolejki.</span><span class="sxs-lookup"><span data-stu-id="93f46-115">This example uses the *Prefix* parameter to get a list of storage queues whose name starts with queue.</span></span>

## <span data-ttu-id="93f46-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="93f46-116">PARAMETERS</span></span>

### <span data-ttu-id="93f46-117">-Context</span><span class="sxs-lookup"><span data-stu-id="93f46-117">-Context</span></span>
<span data-ttu-id="93f46-118">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="93f46-118">Specifies the Azure storage context.</span></span>
<span data-ttu-id="93f46-119">Możesz ją utworzyć przy użyciu polecenia cmdlet **New-AzureStorageContext** .</span><span class="sxs-lookup"><span data-stu-id="93f46-119">You can create it by using the **New-AzureStorageContext** cmdlet.</span></span>

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

### <span data-ttu-id="93f46-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93f46-120">-DefaultProfile</span></span>
<span data-ttu-id="93f46-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="93f46-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93f46-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="93f46-122">-Name</span></span>
<span data-ttu-id="93f46-123">Określa nazwę.</span><span class="sxs-lookup"><span data-stu-id="93f46-123">Specifies a name.</span></span>
<span data-ttu-id="93f46-124">Jeśli nie podano nazwy, polecenie cmdlet powoduje wyświetlenie listy wszystkich kolejek.</span><span class="sxs-lookup"><span data-stu-id="93f46-124">If no name is specified, the cmdlet gets a list of all the queues.</span></span>
<span data-ttu-id="93f46-125">Jeśli jest określona pełna lub częściowa nazwa, polecenie cmdlet pobiera wszystkie kolejki zgodne ze wzorcem nazwy.</span><span class="sxs-lookup"><span data-stu-id="93f46-125">If a full or partial name is specified, the cmdlet gets all queues that match the name pattern.</span></span>

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

### <span data-ttu-id="93f46-126">-Prefix</span><span class="sxs-lookup"><span data-stu-id="93f46-126">-Prefix</span></span>
<span data-ttu-id="93f46-127">Określa prefiks, którego nazwy są używane w nazwach kolejek, które chcesz pobrać.</span><span class="sxs-lookup"><span data-stu-id="93f46-127">Specifies a prefix used in the name of the queues you want to get.</span></span>

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

### <span data-ttu-id="93f46-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93f46-128">CommonParameters</span></span>
<span data-ttu-id="93f46-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93f46-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93f46-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="93f46-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93f46-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="93f46-131">INPUTS</span></span>

### <span data-ttu-id="93f46-132">System. String</span><span class="sxs-lookup"><span data-stu-id="93f46-132">System.String</span></span>

### <span data-ttu-id="93f46-133">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="93f46-133">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="93f46-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="93f46-134">OUTPUTS</span></span>

### <span data-ttu-id="93f46-135">Microsoft. platformy windowsazure. Commands. Common. Storage. ResourceModel. AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="93f46-135">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageQueue</span></span>

## <span data-ttu-id="93f46-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="93f46-136">NOTES</span></span>

## <span data-ttu-id="93f46-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="93f46-137">RELATED LINKS</span></span>

[<span data-ttu-id="93f46-138">Nowe — AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="93f46-138">New-AzureStorageQueue</span></span>](./New-AzureStorageQueue.md)

[<span data-ttu-id="93f46-139">Remove-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="93f46-139">Remove-AzureStorageQueue</span></span>](./Remove-AzureStorageQueue.md)


