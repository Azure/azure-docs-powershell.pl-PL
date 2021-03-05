---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: FF111B74-90A3-4F7C-B515-CE1EEF68EB54
online version: https://docs.microsoft.com/powershell/module/az.batch/new-azbatchapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchApplication.md
ms.openlocfilehash: e22c1ef6a95fafe21f0fd10a47a67098976395e5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101966746"
---
# <span data-ttu-id="29551-101">New-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="29551-101">New-AzBatchApplication</span></span>

## <span data-ttu-id="29551-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="29551-102">SYNOPSIS</span></span>
<span data-ttu-id="29551-103">Dodaje aplikację do określonego konta usługi Batch.</span><span class="sxs-lookup"><span data-stu-id="29551-103">Adds an application to the specified Batch account.</span></span>

## <span data-ttu-id="29551-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="29551-104">SYNTAX</span></span>

```
New-AzBatchApplication [-AccountName] <String> [-ResourceGroupName] <String> [-ApplicationName] <String>
 [[-AllowUpdates] <Boolean>] [[-DisplayName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="29551-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="29551-105">DESCRIPTION</span></span>
<span data-ttu-id="29551-106">Polecenie **cmdlet New-AzBatchApplication** dodaje aplikację do określonego konta usługi Azure Batch.</span><span class="sxs-lookup"><span data-stu-id="29551-106">The **New-AzBatchApplication** cmdlet adds an application to the specified Azure Batch account.</span></span>

## <span data-ttu-id="29551-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="29551-107">EXAMPLES</span></span>

### <span data-ttu-id="29551-108">Przykład 1. Dodawanie pustej aplikacji do konta wsadowego</span><span class="sxs-lookup"><span data-stu-id="29551-108">Example 1: Add an empty application to a Batch account</span></span>
```
PS C:\>New-AzBatchApplication -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationName "Litware" -AllowUpdates $True -DisplayName "Litware Advanced Reticulator"
```

<span data-ttu-id="29551-109">To polecenie tworzy aplikację Litware na koncie ContosoBatch.</span><span class="sxs-lookup"><span data-stu-id="29551-109">This command creates the Litware application in the ContosoBatch account.</span></span>
<span data-ttu-id="29551-110">Początkowo aplikacja nie zawiera żadnych pakietów.</span><span class="sxs-lookup"><span data-stu-id="29551-110">The application initially contains no packages.</span></span>

## <span data-ttu-id="29551-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="29551-111">PARAMETERS</span></span>

### <span data-ttu-id="29551-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="29551-112">-AccountName</span></span>
<span data-ttu-id="29551-113">Określa nazwę konta usługi Batch, do którego to polecenie cmdlet dodaje aplikację.</span><span class="sxs-lookup"><span data-stu-id="29551-113">Specifies the name of the Batch account to which this cmdlet adds an application.</span></span>

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

### <span data-ttu-id="29551-114">-AllowUpdates</span><span class="sxs-lookup"><span data-stu-id="29551-114">-AllowUpdates</span></span>
<span data-ttu-id="29551-115">Określa, czy pakiety w aplikacji mogą być zastępowane przy użyciu tego samego ciągu wersji.</span><span class="sxs-lookup"><span data-stu-id="29551-115">Specifies whether packages within the application can be overwritten using the same version string.</span></span>

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

### <span data-ttu-id="29551-116">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="29551-116">-ApplicationName</span></span>
<span data-ttu-id="29551-117">Określa nazwę aplikacji.</span><span class="sxs-lookup"><span data-stu-id="29551-117">Specifies the name of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ApplicationId

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29551-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29551-118">-DefaultProfile</span></span>
<span data-ttu-id="29551-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="29551-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="29551-120">— DisplayName</span><span class="sxs-lookup"><span data-stu-id="29551-120">-DisplayName</span></span>
<span data-ttu-id="29551-121">Określa nazwę wyświetlaną aplikacji.</span><span class="sxs-lookup"><span data-stu-id="29551-121">Specifies the display name for the application.</span></span>

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

### <span data-ttu-id="29551-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29551-122">-ResourceGroupName</span></span>
<span data-ttu-id="29551-123">Określa nazwę grupy zasobów zawierającej konto Batch.</span><span class="sxs-lookup"><span data-stu-id="29551-123">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="29551-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29551-124">CommonParameters</span></span>
<span data-ttu-id="29551-125">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29551-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29551-126">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="29551-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29551-127">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="29551-127">INPUTS</span></span>

### <span data-ttu-id="29551-128">System.String</span><span class="sxs-lookup"><span data-stu-id="29551-128">System.String</span></span>

### <span data-ttu-id="29551-129">System.Nullable'1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="29551-129">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="29551-130">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="29551-130">OUTPUTS</span></span>

### <span data-ttu-id="29551-131">Microsoft.Azure.Commands.Batch. Models.PSApplication</span><span class="sxs-lookup"><span data-stu-id="29551-131">Microsoft.Azure.Commands.Batch.Models.PSApplication</span></span>

## <span data-ttu-id="29551-132">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="29551-132">NOTES</span></span>

## <span data-ttu-id="29551-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="29551-133">RELATED LINKS</span></span>

[<span data-ttu-id="29551-134">Get-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="29551-134">Get-AzBatchApplication</span></span>](./Get-AzBatchApplication.md)

[<span data-ttu-id="29551-135">Get-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="29551-135">Get-AzBatchApplicationPackage</span></span>](./Get-AzBatchApplicationPackage.md)

[<span data-ttu-id="29551-136">New-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="29551-136">New-AzBatchApplicationPackage</span></span>](./New-AzBatchApplicationPackage.md)

[<span data-ttu-id="29551-137">Remove-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="29551-137">Remove-AzBatchApplication</span></span>](./Remove-AzBatchApplication.md)

[<span data-ttu-id="29551-138">Remove-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="29551-138">Remove-AzBatchApplicationPackage</span></span>](./Remove-AzBatchApplicationPackage.md)

[<span data-ttu-id="29551-139">Set-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="29551-139">Set-AzBatchApplication</span></span>](./Set-AzBatchApplication.md)


