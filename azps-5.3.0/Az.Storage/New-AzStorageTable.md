---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 3B4F32F3-51ED-4851-B38F-172658186C96
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageTable.md
ms.openlocfilehash: 0f46570858368a821d176a5f4e0a907c8a56b49c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98502719"
---
# <span data-ttu-id="2aa61-101">New-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="2aa61-101">New-AzStorageTable</span></span>

## <span data-ttu-id="2aa61-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2aa61-102">SYNOPSIS</span></span>
<span data-ttu-id="2aa61-103">Tworzy tabelę magazynu.</span><span class="sxs-lookup"><span data-stu-id="2aa61-103">Creates a storage table.</span></span>

## <span data-ttu-id="2aa61-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2aa61-104">SYNTAX</span></span>

```
New-AzStorageTable [-Name] <String> [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2aa61-105">Opis</span><span class="sxs-lookup"><span data-stu-id="2aa61-105">DESCRIPTION</span></span>
<span data-ttu-id="2aa61-106">Polecenie cmdlet **New-AzStorageTable** tworzy tabelę magazynu skojarzoną z kontem magazynu na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="2aa61-106">The **New-AzStorageTable** cmdlet creates a storage table associated with the storage account in Azure.</span></span>

## <span data-ttu-id="2aa61-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2aa61-107">EXAMPLES</span></span>

### <span data-ttu-id="2aa61-108">Przykład 1. Tworzenie tabeli magazynu platformy Azure</span><span class="sxs-lookup"><span data-stu-id="2aa61-108">Example 1: Create an azure storage table</span></span>
```
PS C:\>New-AzStorageTable -Name "tableabc"
```

<span data-ttu-id="2aa61-109">To polecenie tworzy tabelę magazynu o nazwie tableabc.</span><span class="sxs-lookup"><span data-stu-id="2aa61-109">This command creates a storage table with a name of tableabc.</span></span>

### <span data-ttu-id="2aa61-110">Przykład 2: Tworzenie wielu tabel magazynu platformy Azure</span><span class="sxs-lookup"><span data-stu-id="2aa61-110">Example 2: Create multiple azure storage tables</span></span>
```
PS C:\>"table1 table2 table3".split() | New-AzStorageTable
```

<span data-ttu-id="2aa61-111">To polecenie powoduje utworzenie wielu tabel.</span><span class="sxs-lookup"><span data-stu-id="2aa61-111">This command creates multiple tables.</span></span>
<span data-ttu-id="2aa61-112">Używa metody **Split** klasy **String** programu .NET, a następnie przekazuje imiona i nazwiska w potoku.</span><span class="sxs-lookup"><span data-stu-id="2aa61-112">It uses the **Split** method of the .NET **String** class and then passes the names on the pipeline.</span></span>

## <span data-ttu-id="2aa61-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2aa61-113">PARAMETERS</span></span>

### <span data-ttu-id="2aa61-114">-Context</span><span class="sxs-lookup"><span data-stu-id="2aa61-114">-Context</span></span>
<span data-ttu-id="2aa61-115">Określa kontekst miejsca do magazynowania.</span><span class="sxs-lookup"><span data-stu-id="2aa61-115">Specifies the storage context.</span></span>
<span data-ttu-id="2aa61-116">Aby ją utworzyć, możesz użyć New-AzStorageContext polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2aa61-116">To create it, you can use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="2aa61-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2aa61-117">-DefaultProfile</span></span>
<span data-ttu-id="2aa61-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2aa61-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2aa61-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="2aa61-119">-Name</span></span>
<span data-ttu-id="2aa61-120">Określa nazwę nowej tabeli.</span><span class="sxs-lookup"><span data-stu-id="2aa61-120">Specifies a name for the new table.</span></span>

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

### <span data-ttu-id="2aa61-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2aa61-121">CommonParameters</span></span>
<span data-ttu-id="2aa61-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2aa61-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2aa61-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2aa61-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2aa61-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2aa61-124">INPUTS</span></span>

### <span data-ttu-id="2aa61-125">System. String</span><span class="sxs-lookup"><span data-stu-id="2aa61-125">System.String</span></span>

### <span data-ttu-id="2aa61-126">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="2aa61-126">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="2aa61-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2aa61-127">OUTPUTS</span></span>

### <span data-ttu-id="2aa61-128">Microsoft. platformy windowsazure. Commands. Common. Storage. ResourceModel. AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="2aa61-128">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageTable</span></span>

## <span data-ttu-id="2aa61-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2aa61-129">NOTES</span></span>

## <span data-ttu-id="2aa61-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2aa61-130">RELATED LINKS</span></span>

[<span data-ttu-id="2aa61-131">Get-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="2aa61-131">Get-AzStorageTable</span></span>](./Get-AzStorageTable.md)

[<span data-ttu-id="2aa61-132">Remove-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="2aa61-132">Remove-AzStorageTable</span></span>](./Remove-AzStorageTable.md)


