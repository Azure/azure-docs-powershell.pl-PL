---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: DCA1FD7A-54AF-48B1-A245-BFA9C43ACA9B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureRmBatchApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureRmBatchApplication.md
ms.openlocfilehash: c1170dc6413c615c7ea1941cc9a446fe2da1610b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93547019"
---
# <span data-ttu-id="0ea15-101">Set-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="0ea15-101">Set-AzureRmBatchApplication</span></span>

## <span data-ttu-id="0ea15-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0ea15-102">SYNOPSIS</span></span>
<span data-ttu-id="0ea15-103">Aktualizuje ustawienia określonej aplikacji.</span><span class="sxs-lookup"><span data-stu-id="0ea15-103">Updates settings for the specified application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0ea15-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0ea15-104">SYNTAX</span></span>

```
Set-AzureRmBatchApplication [-AccountName] <String> [-ResourceGroupName] <String> [-ApplicationId] <String>
 [[-DisplayName] <String>] [[-DefaultVersion] <String>] [[-AllowUpdates] <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0ea15-105">Opis</span><span class="sxs-lookup"><span data-stu-id="0ea15-105">DESCRIPTION</span></span>
<span data-ttu-id="0ea15-106">Polecenie cmdlet **Set-AzureRmBatchApplication** modyfikuje ustawienia określonej aplikacji Azure Batch.</span><span class="sxs-lookup"><span data-stu-id="0ea15-106">The **Set-AzureRmBatchApplication** cmdlet modifies settings for the specified Azure Batch application.</span></span>

## <span data-ttu-id="0ea15-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0ea15-107">EXAMPLES</span></span>

### <span data-ttu-id="0ea15-108">Przykład 1: aktualizowanie aplikacji na koncie wsadowym</span><span class="sxs-lookup"><span data-stu-id="0ea15-108">Example 1: Update an application in a Batch account</span></span>
```
PS C:\>Set-AzureRmBatchApplication -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationId "Litware" -AllowUpdates $False
```

<span data-ttu-id="0ea15-109">To polecenie zmienia, czy aplikacja Llitware na koncie ContosoBatch zezwala na aktualizacje.</span><span class="sxs-lookup"><span data-stu-id="0ea15-109">This command changes whether the Llitware application in the ContosoBatch account allows updates.</span></span>
<span data-ttu-id="0ea15-110">Polecenie nie powoduje zmiany domyślnej wersji ani nazwy wyświetlanej aplikacji.</span><span class="sxs-lookup"><span data-stu-id="0ea15-110">The command does not change the default version or display name of the application.</span></span>

## <span data-ttu-id="0ea15-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0ea15-111">PARAMETERS</span></span>

### <span data-ttu-id="0ea15-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="0ea15-112">-AccountName</span></span>
<span data-ttu-id="0ea15-113">Określa nazwę konta wsadowego, dla którego to polecenie cmdlet modyfikuje aplikację.</span><span class="sxs-lookup"><span data-stu-id="0ea15-113">Specifies the name of the Batch account for which this cmdlet modifies an application.</span></span>

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

### <span data-ttu-id="0ea15-114">-AllowUpdates</span><span class="sxs-lookup"><span data-stu-id="0ea15-114">-AllowUpdates</span></span>
<span data-ttu-id="0ea15-115">Określa, czy pakiety wewnątrz aplikacji mogą być zastępowane przy użyciu tego samego ciągu wersji.</span><span class="sxs-lookup"><span data-stu-id="0ea15-115">Specifies whether packages within the application can be overwritten using the same version string.</span></span>

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

### <span data-ttu-id="0ea15-116">-Identyfikator aplikacji</span><span class="sxs-lookup"><span data-stu-id="0ea15-116">-ApplicationId</span></span>
<span data-ttu-id="0ea15-117">Określa identyfikator aplikacji.</span><span class="sxs-lookup"><span data-stu-id="0ea15-117">Specifies the ID of the application.</span></span>

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

### <span data-ttu-id="0ea15-118">-DefaultVersion</span><span class="sxs-lookup"><span data-stu-id="0ea15-118">-DefaultVersion</span></span>
<span data-ttu-id="0ea15-119">Określa, który pakiet ma być używany, jeśli klient zażąda aplikacji, ale nie określa wersji.</span><span class="sxs-lookup"><span data-stu-id="0ea15-119">Specifies which package to use if a client requests the application but does not specify a version.</span></span>

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

### <span data-ttu-id="0ea15-120">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="0ea15-120">-DisplayName</span></span>
<span data-ttu-id="0ea15-121">Określa nazwę wyświetlaną dla aplikacji.</span><span class="sxs-lookup"><span data-stu-id="0ea15-121">Specifies the display name for the application.</span></span>

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

### <span data-ttu-id="0ea15-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0ea15-122">-ResourceGroupName</span></span>
<span data-ttu-id="0ea15-123">Określa nazwę grupy zasobów zawierającej konto wsadowe.</span><span class="sxs-lookup"><span data-stu-id="0ea15-123">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="0ea15-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ea15-124">-DefaultProfile</span></span>
<span data-ttu-id="0ea15-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0ea15-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0ea15-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ea15-126">CommonParameters</span></span>
<span data-ttu-id="0ea15-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0ea15-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ea15-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0ea15-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ea15-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0ea15-129">INPUTS</span></span>

## <span data-ttu-id="0ea15-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0ea15-130">OUTPUTS</span></span>

## <span data-ttu-id="0ea15-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0ea15-131">NOTES</span></span>

## <span data-ttu-id="0ea15-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0ea15-132">RELATED LINKS</span></span>

[<span data-ttu-id="0ea15-133">Get-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="0ea15-133">Get-AzureRmBatchApplication</span></span>](./Get-AzureRmBatchApplication.md)

[<span data-ttu-id="0ea15-134">Get-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="0ea15-134">Get-AzureRmBatchApplicationPackage</span></span>](./Get-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="0ea15-135">Nowe — AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="0ea15-135">New-AzureRmBatchApplication</span></span>](./New-AzureRmBatchApplication.md)

[<span data-ttu-id="0ea15-136">Nowe — AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="0ea15-136">New-AzureRmBatchApplicationPackage</span></span>](./New-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="0ea15-137">Remove-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="0ea15-137">Remove-AzureRmBatchApplication</span></span>](./Remove-AzureRmBatchApplication.md)

[<span data-ttu-id="0ea15-138">Remove-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="0ea15-138">Remove-AzureRmBatchApplicationPackage</span></span>](./Remove-AzureRmBatchApplicationPackage.md)


