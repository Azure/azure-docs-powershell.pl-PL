---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: AFDE5ECD-29AB-4C91-98BF-1B8C9C3BB079
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchAccountKey.md
ms.openlocfilehash: 46fd2a51e898ec394af4a78370098a479822fc5a
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/13/2020
ms.locfileid: "94061651"
---
# <span data-ttu-id="6ea34-101">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="6ea34-101">Get-AzBatchAccountKey</span></span>

## <span data-ttu-id="6ea34-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6ea34-102">SYNOPSIS</span></span>
<span data-ttu-id="6ea34-103">Pobiera klucze konta wsadowego.</span><span class="sxs-lookup"><span data-stu-id="6ea34-103">Gets the keys of a Batch account.</span></span>

## <span data-ttu-id="6ea34-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6ea34-104">SYNTAX</span></span>

```
Get-AzBatchAccountKey [-AccountName] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6ea34-105">Opis</span><span class="sxs-lookup"><span data-stu-id="6ea34-105">DESCRIPTION</span></span>
<span data-ttu-id="6ea34-106">Polecenie cmdlet **Get-AzBatchAccountKey** pobiera klucze konta usługi Azure Batch w bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="6ea34-106">The **Get-AzBatchAccountKey** cmdlet gets the keys of an Azure Batch account in the current subscription.</span></span>

## <span data-ttu-id="6ea34-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6ea34-107">EXAMPLES</span></span>

### <span data-ttu-id="6ea34-108">Przykład 1: pobieranie kluczy konta partii i zapisywanie ich w $Context zmiennej do późniejszego użycia</span><span class="sxs-lookup"><span data-stu-id="6ea34-108">Example 1: Get batch account keys and save it in $Context variable for use later</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName myaccount
```

<span data-ttu-id="6ea34-109">To polecenie pobiera dane konta i przechowuje je w `$Context` obiekcie do późniejszego użycia.</span><span class="sxs-lookup"><span data-stu-id="6ea34-109">This command gets the account details and stores it in a `$Context` object for use later.</span></span>

### <span data-ttu-id="6ea34-110">Przykład 2: pobieranie kluczy konta wsadowego i wyświetlanie ich</span><span class="sxs-lookup"><span data-stu-id="6ea34-110">Example 2: Get batch account keys and display them</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName myaccount
PS C:\>$Context.PrimaryAccountKey
ABCDEFGHIJKLMNOPQRSTUVWXYZ0123456789ABCDEFGHIJKLMNOPQRSTUVWXYZ0123456789ABCDEFGHIJKLMN==
PS C:\>$Context.SecondaryAccountKey
ABCDEFGHIJKLMNOPQRSTUVWXYZ0123456789ABCDEFGHIJKLMNOPQRSTUVWXYZ0123456789ABCDEFGHIJKLMN==
```

<span data-ttu-id="6ea34-111">To polecenie pobiera klucze kont i drukuje je w konsoli.</span><span class="sxs-lookup"><span data-stu-id="6ea34-111">This command gets the account keys and prints them to the console.</span></span>

## <span data-ttu-id="6ea34-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6ea34-112">PARAMETERS</span></span>

### <span data-ttu-id="6ea34-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="6ea34-113">-AccountName</span></span>
<span data-ttu-id="6ea34-114">Określa nazwę konta, dla którego to polecenie cmdlet pobiera klucze.</span><span class="sxs-lookup"><span data-stu-id="6ea34-114">Specifies the name of the account for which this cmdlet gets keys.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ea34-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ea34-115">-DefaultProfile</span></span>
<span data-ttu-id="6ea34-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6ea34-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6ea34-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ea34-117">-ResourceGroupName</span></span>
<span data-ttu-id="6ea34-118">Określa nazwę grupy zasobów zawierającej konto, dla którego to polecenie cmdlet pobiera klucze.</span><span class="sxs-lookup"><span data-stu-id="6ea34-118">Specifies the name of the resource group that contains the account for which this cmdlet gets keys.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ea34-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ea34-119">CommonParameters</span></span>
<span data-ttu-id="6ea34-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6ea34-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ea34-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6ea34-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ea34-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6ea34-122">INPUTS</span></span>

### <span data-ttu-id="6ea34-123">System. String</span><span class="sxs-lookup"><span data-stu-id="6ea34-123">System.String</span></span>

## <span data-ttu-id="6ea34-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6ea34-124">OUTPUTS</span></span>

### <span data-ttu-id="6ea34-125">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="6ea34-125">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="6ea34-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6ea34-126">NOTES</span></span>

## <span data-ttu-id="6ea34-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6ea34-127">RELATED LINKS</span></span>

[<span data-ttu-id="6ea34-128">Nowe — AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="6ea34-128">New-AzBatchAccountKey</span></span>](./New-AzBatchAccountKey.md)

[<span data-ttu-id="6ea34-129">Polecenia cmdlet usługi Azure Batch</span><span class="sxs-lookup"><span data-stu-id="6ea34-129">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


