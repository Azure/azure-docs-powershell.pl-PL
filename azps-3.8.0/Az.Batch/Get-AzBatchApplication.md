---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: CF8B8E94-3C6C-4D68-B55B-956393890946
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchApplication.md
ms.openlocfilehash: efdcab51a8dfa6d886a317fa1707b65861cf2563
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94053106"
---
# <span data-ttu-id="7fffa-101">Get-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="7fffa-101">Get-AzBatchApplication</span></span>

## <span data-ttu-id="7fffa-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7fffa-102">SYNOPSIS</span></span>
<span data-ttu-id="7fffa-103">Pobiera informacje o określonej aplikacji.</span><span class="sxs-lookup"><span data-stu-id="7fffa-103">Gets information about the specified application.</span></span>

## <span data-ttu-id="7fffa-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7fffa-104">SYNTAX</span></span>

```
Get-AzBatchApplication [-AccountName] <String> [-ResourceGroupName] <String> [[-ApplicationName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7fffa-105">Opis</span><span class="sxs-lookup"><span data-stu-id="7fffa-105">DESCRIPTION</span></span>
<span data-ttu-id="7fffa-106">Polecenie cmdlet **Get-AzBatchApplication** pobiera informacje o aplikacji z konta usługi Azure Batch.</span><span class="sxs-lookup"><span data-stu-id="7fffa-106">The **Get-AzBatchApplication** cmdlet gets information about an application in an Azure Batch account.</span></span>

## <span data-ttu-id="7fffa-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7fffa-107">EXAMPLES</span></span>

### <span data-ttu-id="7fffa-108">Przykład 1. Wyświetlanie aplikacji na koncie wsadowym</span><span class="sxs-lookup"><span data-stu-id="7fffa-108">Example 1: Display the applications in a Batch account</span></span>
```
PS C:\>Get-AzBatchApplication -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup"
ApplicationName AllowUpdates DisplayName

------------- ------------ ----------------------------

litware       False        Litware Advanced Reticulator
```

<span data-ttu-id="7fffa-109">To polecenie wyświetla wszystkie aplikacje na koncie ContosoBatch.</span><span class="sxs-lookup"><span data-stu-id="7fffa-109">This command displays all applications in the ContosoBatch account.</span></span>

## <span data-ttu-id="7fffa-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7fffa-110">PARAMETERS</span></span>

### <span data-ttu-id="7fffa-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="7fffa-111">-AccountName</span></span>
<span data-ttu-id="7fffa-112">Określa nazwę konta wsadowego zawierającego odpowiednią aplikację.</span><span class="sxs-lookup"><span data-stu-id="7fffa-112">Specifies the name of the Batch account that contains the application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7fffa-113">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="7fffa-113">-ApplicationName</span></span>
<span data-ttu-id="7fffa-114">Określa nazwę aplikacji.</span><span class="sxs-lookup"><span data-stu-id="7fffa-114">Specifies the name of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ApplicationId

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7fffa-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7fffa-115">-DefaultProfile</span></span>
<span data-ttu-id="7fffa-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7fffa-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7fffa-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7fffa-117">-ResourceGroupName</span></span>
<span data-ttu-id="7fffa-118">Określa nazwę grupy zasobów zawierającej konto wsadowe.</span><span class="sxs-lookup"><span data-stu-id="7fffa-118">Specifies the name of the resource group that contains the Batch account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7fffa-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7fffa-119">CommonParameters</span></span>
<span data-ttu-id="7fffa-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7fffa-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7fffa-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7fffa-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7fffa-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7fffa-122">INPUTS</span></span>

### <span data-ttu-id="7fffa-123">System. String</span><span class="sxs-lookup"><span data-stu-id="7fffa-123">System.String</span></span>

## <span data-ttu-id="7fffa-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7fffa-124">OUTPUTS</span></span>

### <span data-ttu-id="7fffa-125">Microsoft.Azure.Commands.Batch. Modele. PSApplication</span><span class="sxs-lookup"><span data-stu-id="7fffa-125">Microsoft.Azure.Commands.Batch.Models.PSApplication</span></span>

## <span data-ttu-id="7fffa-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7fffa-126">NOTES</span></span>

## <span data-ttu-id="7fffa-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7fffa-127">RELATED LINKS</span></span>

[<span data-ttu-id="7fffa-128">Get-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="7fffa-128">Get-AzBatchApplicationPackage</span></span>](./Get-AzBatchApplicationPackage.md)

[<span data-ttu-id="7fffa-129">Nowe — AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="7fffa-129">New-AzBatchApplication</span></span>](./New-AzBatchApplication.md)

[<span data-ttu-id="7fffa-130">Nowe — AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="7fffa-130">New-AzBatchApplicationPackage</span></span>](./New-AzBatchApplicationPackage.md)

[<span data-ttu-id="7fffa-131">Remove-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="7fffa-131">Remove-AzBatchApplication</span></span>](./Remove-AzBatchApplication.md)

[<span data-ttu-id="7fffa-132">Remove-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="7fffa-132">Remove-AzBatchApplicationPackage</span></span>](./Remove-AzBatchApplicationPackage.md)

[<span data-ttu-id="7fffa-133">Set-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="7fffa-133">Set-AzBatchApplication</span></span>](./Set-AzBatchApplication.md)


