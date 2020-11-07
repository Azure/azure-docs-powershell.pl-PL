---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: FF111B74-90A3-4F7C-B515-CE1EEF68EB54
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/new-azbatchapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchApplication.md
ms.openlocfilehash: 0c1d847045cc4fb8be39674c13c38114ee9d3a57
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93706661"
---
# <span data-ttu-id="75dfc-101">New-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="75dfc-101">New-AzBatchApplication</span></span>

## <span data-ttu-id="75dfc-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="75dfc-102">SYNOPSIS</span></span>
<span data-ttu-id="75dfc-103">Dodaje aplikację do określonego konta wsadowego.</span><span class="sxs-lookup"><span data-stu-id="75dfc-103">Adds an application to the specified Batch account.</span></span>

## <span data-ttu-id="75dfc-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="75dfc-104">SYNTAX</span></span>

```
New-AzBatchApplication [-AccountName] <String> [-ResourceGroupName] <String> [-ApplicationId] <String>
 [[-AllowUpdates] <Boolean>] [[-DisplayName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="75dfc-105">Opis</span><span class="sxs-lookup"><span data-stu-id="75dfc-105">DESCRIPTION</span></span>
<span data-ttu-id="75dfc-106">Polecenie cmdlet **New-AzBatchApplication** umożliwia dodanie aplikacji do określonego konta usługi Azure Batch.</span><span class="sxs-lookup"><span data-stu-id="75dfc-106">The **New-AzBatchApplication** cmdlet adds an application to the specified Azure Batch account.</span></span>

## <span data-ttu-id="75dfc-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="75dfc-107">EXAMPLES</span></span>

### <span data-ttu-id="75dfc-108">Przykład 1: Dodawanie pustej aplikacji do konta partii</span><span class="sxs-lookup"><span data-stu-id="75dfc-108">Example 1: Add an empty application to a Batch account</span></span>
```
PS C:\>New-AzBatchApplication -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationId "Litware" -AllowUpdates $True -DisplayName "Litware Advanced Reticulator"
```

<span data-ttu-id="75dfc-109">To polecenie tworzy aplikację Przykładowa na koncie ContosoBatch.</span><span class="sxs-lookup"><span data-stu-id="75dfc-109">This command creates the Litware application in the ContosoBatch account.</span></span>
<span data-ttu-id="75dfc-110">Aplikacja początkowo nie zawiera żadnych pakietów.</span><span class="sxs-lookup"><span data-stu-id="75dfc-110">The application initially contains no packages.</span></span>

## <span data-ttu-id="75dfc-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="75dfc-111">PARAMETERS</span></span>

### <span data-ttu-id="75dfc-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="75dfc-112">-AccountName</span></span>
<span data-ttu-id="75dfc-113">Określa nazwę konta wsadowego, do którego jest dodawana aplikacja.</span><span class="sxs-lookup"><span data-stu-id="75dfc-113">Specifies the name of the Batch account to which this cmdlet adds an application.</span></span>

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

### <span data-ttu-id="75dfc-114">-AllowUpdates</span><span class="sxs-lookup"><span data-stu-id="75dfc-114">-AllowUpdates</span></span>
<span data-ttu-id="75dfc-115">Określa, czy pakiety wewnątrz aplikacji mogą być zastępowane przy użyciu tego samego ciągu wersji.</span><span class="sxs-lookup"><span data-stu-id="75dfc-115">Specifies whether packages within the application can be overwritten using the same version string.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75dfc-116">-Identyfikator aplikacji</span><span class="sxs-lookup"><span data-stu-id="75dfc-116">-ApplicationId</span></span>
<span data-ttu-id="75dfc-117">Określa identyfikator aplikacji.</span><span class="sxs-lookup"><span data-stu-id="75dfc-117">Specifies the ID of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75dfc-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75dfc-118">-DefaultProfile</span></span>
<span data-ttu-id="75dfc-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="75dfc-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="75dfc-120">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="75dfc-120">-DisplayName</span></span>
<span data-ttu-id="75dfc-121">Określa nazwę wyświetlaną dla aplikacji.</span><span class="sxs-lookup"><span data-stu-id="75dfc-121">Specifies the display name for the application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75dfc-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75dfc-122">-ResourceGroupName</span></span>
<span data-ttu-id="75dfc-123">Określa nazwę grupy zasobów zawierającej konto wsadowe.</span><span class="sxs-lookup"><span data-stu-id="75dfc-123">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="75dfc-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75dfc-124">CommonParameters</span></span>
<span data-ttu-id="75dfc-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75dfc-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75dfc-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75dfc-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75dfc-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="75dfc-127">INPUTS</span></span>

### <span data-ttu-id="75dfc-128">System. String</span><span class="sxs-lookup"><span data-stu-id="75dfc-128">System.String</span></span>

### <span data-ttu-id="75dfc-129">System. Nullable "1 [[System. Boolean, system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="75dfc-129">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="75dfc-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="75dfc-130">OUTPUTS</span></span>

### <span data-ttu-id="75dfc-131">Microsoft.Azure.Commands.Batch. Modele. PSApplication</span><span class="sxs-lookup"><span data-stu-id="75dfc-131">Microsoft.Azure.Commands.Batch.Models.PSApplication</span></span>

## <span data-ttu-id="75dfc-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="75dfc-132">NOTES</span></span>

## <span data-ttu-id="75dfc-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="75dfc-133">RELATED LINKS</span></span>

[<span data-ttu-id="75dfc-134">Get-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="75dfc-134">Get-AzBatchApplication</span></span>](./Get-AzBatchApplication.md)

[<span data-ttu-id="75dfc-135">Get-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="75dfc-135">Get-AzBatchApplicationPackage</span></span>](./Get-AzBatchApplicationPackage.md)

[<span data-ttu-id="75dfc-136">Nowe — AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="75dfc-136">New-AzBatchApplicationPackage</span></span>](./New-AzBatchApplicationPackage.md)

[<span data-ttu-id="75dfc-137">Remove-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="75dfc-137">Remove-AzBatchApplication</span></span>](./Remove-AzBatchApplication.md)

[<span data-ttu-id="75dfc-138">Remove-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="75dfc-138">Remove-AzBatchApplicationPackage</span></span>](./Remove-AzBatchApplicationPackage.md)

[<span data-ttu-id="75dfc-139">Set-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="75dfc-139">Set-AzBatchApplication</span></span>](./Set-AzBatchApplication.md)


