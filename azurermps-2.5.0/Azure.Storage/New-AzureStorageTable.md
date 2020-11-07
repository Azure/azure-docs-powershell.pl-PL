---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 3B4F32F3-51ED-4851-B38F-172658186C96
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestoragetable
schema: 2.0.0
ms.openlocfilehash: 4fe02c9824945593de4b4160e9db10b1573a335a
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93898593"
---
# <span data-ttu-id="cfc93-101">New-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="cfc93-101">New-AzureStorageTable</span></span>

## <span data-ttu-id="cfc93-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="cfc93-102">SYNOPSIS</span></span>
<span data-ttu-id="cfc93-103">Tworzy tabelę magazynu.</span><span class="sxs-lookup"><span data-stu-id="cfc93-103">Creates a storage table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cfc93-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="cfc93-104">SYNTAX</span></span>

```
New-AzureStorageTable [-Name] <String> [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="cfc93-105">Opis</span><span class="sxs-lookup"><span data-stu-id="cfc93-105">DESCRIPTION</span></span>
<span data-ttu-id="cfc93-106">Polecenie cmdlet **New-AzureStorageTable** tworzy tabelę magazynu skojarzoną z kontem magazynu na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="cfc93-106">The **New-AzureStorageTable** cmdlet creates a storage table associated with the storage account in Azure.</span></span>

## <span data-ttu-id="cfc93-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="cfc93-107">EXAMPLES</span></span>

### <span data-ttu-id="cfc93-108">Przykład 1. Tworzenie tabeli magazynu platformy Azure</span><span class="sxs-lookup"><span data-stu-id="cfc93-108">Example 1: Create an azure storage table</span></span>
```
PS C:\>New-AzureStorageTable -Name "tableabc"
```

<span data-ttu-id="cfc93-109">To polecenie tworzy tabelę magazynu o nazwie tableabc.</span><span class="sxs-lookup"><span data-stu-id="cfc93-109">This command creates a storage table with a name of tableabc.</span></span>

### <span data-ttu-id="cfc93-110">Przykład 2: Tworzenie wielu tabel magazynu platformy Azure</span><span class="sxs-lookup"><span data-stu-id="cfc93-110">Example 2: Create multiple azure storage tables</span></span>
```
PS C:\>"table1 table2 table3".split() | New-AzureStorageTable
```

<span data-ttu-id="cfc93-111">To polecenie powoduje utworzenie wielu tabel.</span><span class="sxs-lookup"><span data-stu-id="cfc93-111">This command creates multiple tables.</span></span>
<span data-ttu-id="cfc93-112">Używa metody **Split** klasy **String** programu .NET, a następnie przekazuje imiona i nazwiska w potoku.</span><span class="sxs-lookup"><span data-stu-id="cfc93-112">It uses the **Split** method of the .NET **String** class and then passes the names on the pipeline.</span></span>

## <span data-ttu-id="cfc93-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="cfc93-113">PARAMETERS</span></span>

### <span data-ttu-id="cfc93-114">-Context</span><span class="sxs-lookup"><span data-stu-id="cfc93-114">-Context</span></span>
<span data-ttu-id="cfc93-115">Określa kontekst miejsca do magazynowania.</span><span class="sxs-lookup"><span data-stu-id="cfc93-115">Specifies the storage context.</span></span>
<span data-ttu-id="cfc93-116">Aby ją utworzyć, możesz użyć New-AzureStorageContext polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cfc93-116">To create it, you can use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="cfc93-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cfc93-117">-DefaultProfile</span></span>
<span data-ttu-id="cfc93-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="cfc93-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cfc93-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="cfc93-119">-Name</span></span>
<span data-ttu-id="cfc93-120">Określa nazwę nowej tabeli.</span><span class="sxs-lookup"><span data-stu-id="cfc93-120">Specifies a name for the new table.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Table

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cfc93-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cfc93-121">CommonParameters</span></span>
<span data-ttu-id="cfc93-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cfc93-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cfc93-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cfc93-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cfc93-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cfc93-124">INPUTS</span></span>

### <span data-ttu-id="cfc93-125">System. String</span><span class="sxs-lookup"><span data-stu-id="cfc93-125">System.String</span></span>

### <span data-ttu-id="cfc93-126">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="cfc93-126">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="cfc93-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="cfc93-127">OUTPUTS</span></span>

### <span data-ttu-id="cfc93-128">Microsoft. platformy windowsazure. Commands. Common. Storage. ResourceModel. AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="cfc93-128">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageTable</span></span>

## <span data-ttu-id="cfc93-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="cfc93-129">NOTES</span></span>

## <span data-ttu-id="cfc93-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cfc93-130">RELATED LINKS</span></span>

[<span data-ttu-id="cfc93-131">Get-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="cfc93-131">Get-AzureStorageTable</span></span>](./Get-AzureStorageTable.md)

[<span data-ttu-id="cfc93-132">Remove-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="cfc93-132">Remove-AzureStorageTable</span></span>](./Remove-AzureStorageTable.md)


