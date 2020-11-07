---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: E9500392-6BE1-46EC-9AF5-9234281025E6
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragequeue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageQueue.md
ms.openlocfilehash: df6f616aacb066ec17aa089b8d91226a5bd171b8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93707573"
---
# <span data-ttu-id="dd8e7-101">New-AzStorageQueue</span><span class="sxs-lookup"><span data-stu-id="dd8e7-101">New-AzStorageQueue</span></span>

## <span data-ttu-id="dd8e7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="dd8e7-102">SYNOPSIS</span></span>
<span data-ttu-id="dd8e7-103">Umożliwia utworzenie kolejki magazynu.</span><span class="sxs-lookup"><span data-stu-id="dd8e7-103">Creates a storage queue.</span></span>

## <span data-ttu-id="dd8e7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="dd8e7-104">SYNTAX</span></span>

```
New-AzStorageQueue [-Name] <String> [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="dd8e7-105">Opis</span><span class="sxs-lookup"><span data-stu-id="dd8e7-105">DESCRIPTION</span></span>
<span data-ttu-id="dd8e7-106">Polecenie cmdlet **New-AzStorageQueue** tworzy kolejkę magazynowania na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="dd8e7-106">The **New-AzStorageQueue** cmdlet creates a storage queue in Azure.</span></span>

## <span data-ttu-id="dd8e7-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="dd8e7-107">EXAMPLES</span></span>

### <span data-ttu-id="dd8e7-108">Przykład 1. Tworzenie kolejki magazynu platformy Azure</span><span class="sxs-lookup"><span data-stu-id="dd8e7-108">Example 1: Create an Azure storage queue</span></span>
```
PS C:\>New-AzStorageQueue -Name "queueabc"
```

<span data-ttu-id="dd8e7-109">W tym przykładzie jest tworzona Kolejka magazynu o nazwie queueabc.</span><span class="sxs-lookup"><span data-stu-id="dd8e7-109">This example creates a storage queue named queueabc.</span></span>

### <span data-ttu-id="dd8e7-110">Przykład 2: Tworzenie wielu kolejek magazynu platformy Azure</span><span class="sxs-lookup"><span data-stu-id="dd8e7-110">Example 2: Create multiple azure storage queues</span></span>
```
PS C:\>"queue1 queue2 queue3".split() | New-AzStorageQueue
```

<span data-ttu-id="dd8e7-111">W tym przykładzie przedstawiono tworzenie wielu kolejek magazynowych.</span><span class="sxs-lookup"><span data-stu-id="dd8e7-111">This example creates multiple storage queues.</span></span>
<span data-ttu-id="dd8e7-112">Używa metody Split klasy String programu .NET, a następnie przekazuje imiona i nazwiska w potoku.</span><span class="sxs-lookup"><span data-stu-id="dd8e7-112">It uses the Split method of the .NET String class and then passes the names on the pipeline.</span></span>

## <span data-ttu-id="dd8e7-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="dd8e7-113">PARAMETERS</span></span>

### <span data-ttu-id="dd8e7-114">-Context</span><span class="sxs-lookup"><span data-stu-id="dd8e7-114">-Context</span></span>
<span data-ttu-id="dd8e7-115">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="dd8e7-115">Specifies the Azure storage context.</span></span>
<span data-ttu-id="dd8e7-116">Możesz ją utworzyć przy użyciu polecenia cmdlet New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="dd8e7-116">You can create it by using the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="dd8e7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd8e7-117">-DefaultProfile</span></span>
<span data-ttu-id="dd8e7-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="dd8e7-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dd8e7-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="dd8e7-119">-Name</span></span>
<span data-ttu-id="dd8e7-120">Określa nazwę kolejki.</span><span class="sxs-lookup"><span data-stu-id="dd8e7-120">Specifies a name for the queue.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Queue

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dd8e7-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd8e7-121">CommonParameters</span></span>
<span data-ttu-id="dd8e7-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd8e7-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd8e7-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dd8e7-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd8e7-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dd8e7-124">INPUTS</span></span>

### <span data-ttu-id="dd8e7-125">System. String</span><span class="sxs-lookup"><span data-stu-id="dd8e7-125">System.String</span></span>

### <span data-ttu-id="dd8e7-126">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="dd8e7-126">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="dd8e7-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="dd8e7-127">OUTPUTS</span></span>

### <span data-ttu-id="dd8e7-128">Microsoft. platformy windowsazure. Commands. Common. Storage. ResourceModel. AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="dd8e7-128">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageQueue</span></span>

## <span data-ttu-id="dd8e7-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="dd8e7-129">NOTES</span></span>

## <span data-ttu-id="dd8e7-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="dd8e7-130">RELATED LINKS</span></span>

[<span data-ttu-id="dd8e7-131">Get-AzStorageQueue</span><span class="sxs-lookup"><span data-stu-id="dd8e7-131">Get-AzStorageQueue</span></span>](./Get-AzStorageQueue.md)

[<span data-ttu-id="dd8e7-132">Remove-AzStorageQueue</span><span class="sxs-lookup"><span data-stu-id="dd8e7-132">Remove-AzStorageQueue</span></span>](./Remove-AzStorageQueue.md)

