---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: DCA1FD7A-54AF-48B1-A245-BFA9C43ACA9B
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/set-azbatchapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchApplication.md
ms.openlocfilehash: 3dcbd81452ff9c4e5cf029b9c5d6169832d27a62
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93710420"
---
# <span data-ttu-id="2f037-101">Set-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="2f037-101">Set-AzBatchApplication</span></span>

## <span data-ttu-id="2f037-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2f037-102">SYNOPSIS</span></span>
<span data-ttu-id="2f037-103">Aktualizuje ustawienia określonej aplikacji.</span><span class="sxs-lookup"><span data-stu-id="2f037-103">Updates settings for the specified application.</span></span>

## <span data-ttu-id="2f037-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2f037-104">SYNTAX</span></span>

```
Set-AzBatchApplication [-AccountName] <String> [-ResourceGroupName] <String> [-ApplicationId] <String>
 [[-DisplayName] <String>] [[-DefaultVersion] <String>] [[-AllowUpdates] <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2f037-105">Opis</span><span class="sxs-lookup"><span data-stu-id="2f037-105">DESCRIPTION</span></span>
<span data-ttu-id="2f037-106">Polecenie cmdlet **Set-AzBatchApplication** modyfikuje ustawienia określonej aplikacji Azure Batch.</span><span class="sxs-lookup"><span data-stu-id="2f037-106">The **Set-AzBatchApplication** cmdlet modifies settings for the specified Azure Batch application.</span></span>

## <span data-ttu-id="2f037-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2f037-107">EXAMPLES</span></span>

### <span data-ttu-id="2f037-108">Przykład 1: aktualizowanie aplikacji na koncie wsadowym</span><span class="sxs-lookup"><span data-stu-id="2f037-108">Example 1: Update an application in a Batch account</span></span>
```
PS C:\>Set-AzBatchApplication -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationId "Litware" -AllowUpdates $False
```

<span data-ttu-id="2f037-109">To polecenie zmienia, czy aplikacja Llitware na koncie ContosoBatch zezwala na aktualizacje.</span><span class="sxs-lookup"><span data-stu-id="2f037-109">This command changes whether the Llitware application in the ContosoBatch account allows updates.</span></span>
<span data-ttu-id="2f037-110">Polecenie nie powoduje zmiany domyślnej wersji ani nazwy wyświetlanej aplikacji.</span><span class="sxs-lookup"><span data-stu-id="2f037-110">The command does not change the default version or display name of the application.</span></span>

## <span data-ttu-id="2f037-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2f037-111">PARAMETERS</span></span>

### <span data-ttu-id="2f037-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="2f037-112">-AccountName</span></span>
<span data-ttu-id="2f037-113">Określa nazwę konta wsadowego, dla którego to polecenie cmdlet modyfikuje aplikację.</span><span class="sxs-lookup"><span data-stu-id="2f037-113">Specifies the name of the Batch account for which this cmdlet modifies an application.</span></span>

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

### <span data-ttu-id="2f037-114">-AllowUpdates</span><span class="sxs-lookup"><span data-stu-id="2f037-114">-AllowUpdates</span></span>
<span data-ttu-id="2f037-115">Określa, czy pakiety wewnątrz aplikacji mogą być zastępowane przy użyciu tego samego ciągu wersji.</span><span class="sxs-lookup"><span data-stu-id="2f037-115">Specifies whether packages within the application can be overwritten using the same version string.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f037-116">-Identyfikator aplikacji</span><span class="sxs-lookup"><span data-stu-id="2f037-116">-ApplicationId</span></span>
<span data-ttu-id="2f037-117">Określa identyfikator aplikacji.</span><span class="sxs-lookup"><span data-stu-id="2f037-117">Specifies the ID of the application.</span></span>

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

### <span data-ttu-id="2f037-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f037-118">-DefaultProfile</span></span>
<span data-ttu-id="2f037-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2f037-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2f037-120">-DefaultVersion</span><span class="sxs-lookup"><span data-stu-id="2f037-120">-DefaultVersion</span></span>
<span data-ttu-id="2f037-121">Określa, który pakiet ma być używany, jeśli klient zażąda aplikacji, ale nie określa wersji.</span><span class="sxs-lookup"><span data-stu-id="2f037-121">Specifies which package to use if a client requests the application but does not specify a version.</span></span>

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

### <span data-ttu-id="2f037-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="2f037-122">-DisplayName</span></span>
<span data-ttu-id="2f037-123">Określa nazwę wyświetlaną dla aplikacji.</span><span class="sxs-lookup"><span data-stu-id="2f037-123">Specifies the display name for the application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f037-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2f037-124">-ResourceGroupName</span></span>
<span data-ttu-id="2f037-125">Określa nazwę grupy zasobów zawierającej konto wsadowe.</span><span class="sxs-lookup"><span data-stu-id="2f037-125">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="2f037-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f037-126">CommonParameters</span></span>
<span data-ttu-id="2f037-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2f037-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f037-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2f037-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f037-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2f037-129">INPUTS</span></span>

### <span data-ttu-id="2f037-130">System. String</span><span class="sxs-lookup"><span data-stu-id="2f037-130">System.String</span></span>

### <span data-ttu-id="2f037-131">System. Nullable "1 [[System. Boolean, system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="2f037-131">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="2f037-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2f037-132">OUTPUTS</span></span>

### <span data-ttu-id="2f037-133">System. void</span><span class="sxs-lookup"><span data-stu-id="2f037-133">System.Void</span></span>

## <span data-ttu-id="2f037-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2f037-134">NOTES</span></span>

## <span data-ttu-id="2f037-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2f037-135">RELATED LINKS</span></span>

[<span data-ttu-id="2f037-136">Get-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="2f037-136">Get-AzBatchApplication</span></span>](./Get-AzBatchApplication.md)

[<span data-ttu-id="2f037-137">Get-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="2f037-137">Get-AzBatchApplicationPackage</span></span>](./Get-AzBatchApplicationPackage.md)

[<span data-ttu-id="2f037-138">Nowe — AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="2f037-138">New-AzBatchApplication</span></span>](./New-AzBatchApplication.md)

[<span data-ttu-id="2f037-139">Nowe — AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="2f037-139">New-AzBatchApplicationPackage</span></span>](./New-AzBatchApplicationPackage.md)

[<span data-ttu-id="2f037-140">Remove-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="2f037-140">Remove-AzBatchApplication</span></span>](./Remove-AzBatchApplication.md)

[<span data-ttu-id="2f037-141">Remove-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="2f037-141">Remove-AzBatchApplicationPackage</span></span>](./Remove-AzBatchApplicationPackage.md)

