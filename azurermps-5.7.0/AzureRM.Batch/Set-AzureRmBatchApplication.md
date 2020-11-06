---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: DCA1FD7A-54AF-48B1-A245-BFA9C43ACA9B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/set-azurermbatchapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureRmBatchApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureRmBatchApplication.md
ms.openlocfilehash: 157e7a3ee0cc7ea4a80517bf98d17c05df8c7899
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527070"
---
# <span data-ttu-id="4a233-101">Set-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="4a233-101">Set-AzureRmBatchApplication</span></span>

## <span data-ttu-id="4a233-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4a233-102">SYNOPSIS</span></span>
<span data-ttu-id="4a233-103">Aktualizuje ustawienia określonej aplikacji.</span><span class="sxs-lookup"><span data-stu-id="4a233-103">Updates settings for the specified application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4a233-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4a233-104">SYNTAX</span></span>

```
Set-AzureRmBatchApplication [-AccountName] <String> [-ResourceGroupName] <String> [-ApplicationId] <String>
 [[-DisplayName] <String>] [[-DefaultVersion] <String>] [[-AllowUpdates] <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4a233-105">Opis</span><span class="sxs-lookup"><span data-stu-id="4a233-105">DESCRIPTION</span></span>
<span data-ttu-id="4a233-106">Polecenie cmdlet **Set-AzureRmBatchApplication** modyfikuje ustawienia określonej aplikacji Azure Batch.</span><span class="sxs-lookup"><span data-stu-id="4a233-106">The **Set-AzureRmBatchApplication** cmdlet modifies settings for the specified Azure Batch application.</span></span>

## <span data-ttu-id="4a233-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4a233-107">EXAMPLES</span></span>

### <span data-ttu-id="4a233-108">Przykład 1: aktualizowanie aplikacji na koncie wsadowym</span><span class="sxs-lookup"><span data-stu-id="4a233-108">Example 1: Update an application in a Batch account</span></span>
```
PS C:\>Set-AzureRmBatchApplication -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationId "Litware" -AllowUpdates $False
```

<span data-ttu-id="4a233-109">To polecenie zmienia, czy aplikacja Llitware na koncie ContosoBatch zezwala na aktualizacje.</span><span class="sxs-lookup"><span data-stu-id="4a233-109">This command changes whether the Llitware application in the ContosoBatch account allows updates.</span></span>
<span data-ttu-id="4a233-110">Polecenie nie powoduje zmiany domyślnej wersji ani nazwy wyświetlanej aplikacji.</span><span class="sxs-lookup"><span data-stu-id="4a233-110">The command does not change the default version or display name of the application.</span></span>

## <span data-ttu-id="4a233-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4a233-111">PARAMETERS</span></span>

### <span data-ttu-id="4a233-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="4a233-112">-AccountName</span></span>
<span data-ttu-id="4a233-113">Określa nazwę konta wsadowego, dla którego to polecenie cmdlet modyfikuje aplikację.</span><span class="sxs-lookup"><span data-stu-id="4a233-113">Specifies the name of the Batch account for which this cmdlet modifies an application.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a233-114">-AllowUpdates</span><span class="sxs-lookup"><span data-stu-id="4a233-114">-AllowUpdates</span></span>
<span data-ttu-id="4a233-115">Określa, czy pakiety wewnątrz aplikacji mogą być zastępowane przy użyciu tego samego ciągu wersji.</span><span class="sxs-lookup"><span data-stu-id="4a233-115">Specifies whether packages within the application can be overwritten using the same version string.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a233-116">-Identyfikator aplikacji</span><span class="sxs-lookup"><span data-stu-id="4a233-116">-ApplicationId</span></span>
<span data-ttu-id="4a233-117">Określa identyfikator aplikacji.</span><span class="sxs-lookup"><span data-stu-id="4a233-117">Specifies the ID of the application.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a233-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a233-118">-DefaultProfile</span></span>
<span data-ttu-id="4a233-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4a233-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a233-120">-DefaultVersion</span><span class="sxs-lookup"><span data-stu-id="4a233-120">-DefaultVersion</span></span>
<span data-ttu-id="4a233-121">Określa, który pakiet ma być używany, jeśli klient zażąda aplikacji, ale nie określa wersji.</span><span class="sxs-lookup"><span data-stu-id="4a233-121">Specifies which package to use if a client requests the application but does not specify a version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a233-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="4a233-122">-DisplayName</span></span>
<span data-ttu-id="4a233-123">Określa nazwę wyświetlaną dla aplikacji.</span><span class="sxs-lookup"><span data-stu-id="4a233-123">Specifies the display name for the application.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a233-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a233-124">-ResourceGroupName</span></span>
<span data-ttu-id="4a233-125">Określa nazwę grupy zasobów zawierającej konto wsadowe.</span><span class="sxs-lookup"><span data-stu-id="4a233-125">Specifies the name of the resource group that contains the Batch account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a233-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a233-126">CommonParameters</span></span>
<span data-ttu-id="4a233-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4a233-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a233-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4a233-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a233-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4a233-129">INPUTS</span></span>

### <span data-ttu-id="4a233-130">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="4a233-130">None</span></span>
<span data-ttu-id="4a233-131">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="4a233-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4a233-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4a233-132">OUTPUTS</span></span>

## <span data-ttu-id="4a233-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4a233-133">NOTES</span></span>

## <span data-ttu-id="4a233-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4a233-134">RELATED LINKS</span></span>

[<span data-ttu-id="4a233-135">Get-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="4a233-135">Get-AzureRmBatchApplication</span></span>](./Get-AzureRmBatchApplication.md)

[<span data-ttu-id="4a233-136">Get-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="4a233-136">Get-AzureRmBatchApplicationPackage</span></span>](./Get-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="4a233-137">Nowe — AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="4a233-137">New-AzureRmBatchApplication</span></span>](./New-AzureRmBatchApplication.md)

[<span data-ttu-id="4a233-138">Nowe — AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="4a233-138">New-AzureRmBatchApplicationPackage</span></span>](./New-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="4a233-139">Remove-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="4a233-139">Remove-AzureRmBatchApplication</span></span>](./Remove-AzureRmBatchApplication.md)

[<span data-ttu-id="4a233-140">Remove-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="4a233-140">Remove-AzureRmBatchApplicationPackage</span></span>](./Remove-AzureRmBatchApplicationPackage.md)


