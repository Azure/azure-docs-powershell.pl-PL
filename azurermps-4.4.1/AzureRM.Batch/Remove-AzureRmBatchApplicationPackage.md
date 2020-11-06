---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: FD2E3442-9CEA-4390-BE9C-772C7D6FD1E2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureRmBatchApplicationPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureRmBatchApplicationPackage.md
ms.openlocfilehash: 8ef7ba1c678c09ba10bd87c301a417600f51fe0c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93548364"
---
# <span data-ttu-id="4a0d6-101">Remove-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="4a0d6-101">Remove-AzureRmBatchApplicationPackage</span></span>

## <span data-ttu-id="4a0d6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4a0d6-102">SYNOPSIS</span></span>
<span data-ttu-id="4a0d6-103">Usuwa rekord pakietu aplikacji i plik binarny.</span><span class="sxs-lookup"><span data-stu-id="4a0d6-103">Deletes an application package record and the binary file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4a0d6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4a0d6-104">SYNTAX</span></span>

```
Remove-AzureRmBatchApplicationPackage [-AccountName] <String> [-ResourceGroupName] <String>
 [-ApplicationId] <String> [-ApplicationVersion] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4a0d6-105">Opis</span><span class="sxs-lookup"><span data-stu-id="4a0d6-105">DESCRIPTION</span></span>
<span data-ttu-id="4a0d6-106">Polecenie cmdlet **Remove-AzureRmBatchApplicationPackage** usuwa rekord pakietu aplikacji i plik binarny z konta usługi Azure Batch.</span><span class="sxs-lookup"><span data-stu-id="4a0d6-106">The **Remove-AzureRmBatchApplicationPackage** cmdlet deletes an application package record and the binary file from an Azure Batch account.</span></span>

## <span data-ttu-id="4a0d6-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4a0d6-107">EXAMPLES</span></span>

### <span data-ttu-id="4a0d6-108">Przykład 1: Usuwanie pakietu aplikacji z konta partii</span><span class="sxs-lookup"><span data-stu-id="4a0d6-108">Example 1: Delete an application package from a Batch account</span></span>
```
PS C:\>Remove-AzureRmBatchApplicationPackage -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationId "litware" -ApplicationVersion "1.0"
```

<span data-ttu-id="4a0d6-109">To polecenie usuwa wersję 1,0 aplikacji Przykładowa z konta ContosoBatchGroup.</span><span class="sxs-lookup"><span data-stu-id="4a0d6-109">This command deletes version 1.0 of the Litware application from the ContosoBatchGroup account.</span></span>
<span data-ttu-id="4a0d6-110">Polecenie usunie zarówno rekord pakietu, jak i obiekt BLOB zawierający plik binarny pakietu.</span><span class="sxs-lookup"><span data-stu-id="4a0d6-110">The command deletes both the package record and the blob that contain the package binary file.</span></span>

## <span data-ttu-id="4a0d6-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4a0d6-111">PARAMETERS</span></span>

### <span data-ttu-id="4a0d6-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="4a0d6-112">-AccountName</span></span>
<span data-ttu-id="4a0d6-113">Określa nazwę konta wsadowego, z którego to polecenie cmdlet usuwa pakiet aplikacji.</span><span class="sxs-lookup"><span data-stu-id="4a0d6-113">Specifies the name of the Batch account from which this cmdlet deletes an application package.</span></span>

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

### <span data-ttu-id="4a0d6-114">-Identyfikator aplikacji</span><span class="sxs-lookup"><span data-stu-id="4a0d6-114">-ApplicationId</span></span>
<span data-ttu-id="4a0d6-115">Określa identyfikator aplikacji.</span><span class="sxs-lookup"><span data-stu-id="4a0d6-115">Specifies the ID of the application.</span></span>

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

### <span data-ttu-id="4a0d6-116">-ApplicationVersion</span><span class="sxs-lookup"><span data-stu-id="4a0d6-116">-ApplicationVersion</span></span>
<span data-ttu-id="4a0d6-117">Określa wersję aplikacji.</span><span class="sxs-lookup"><span data-stu-id="4a0d6-117">Specifies the version of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a0d6-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a0d6-118">-ResourceGroupName</span></span>
<span data-ttu-id="4a0d6-119">Określa nazwę grupy zasobów zawierającej konto wsadowe.</span><span class="sxs-lookup"><span data-stu-id="4a0d6-119">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="4a0d6-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a0d6-120">-DefaultProfile</span></span>
<span data-ttu-id="4a0d6-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4a0d6-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4a0d6-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a0d6-122">CommonParameters</span></span>
<span data-ttu-id="4a0d6-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4a0d6-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a0d6-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4a0d6-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a0d6-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4a0d6-125">INPUTS</span></span>

## <span data-ttu-id="4a0d6-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4a0d6-126">OUTPUTS</span></span>

## <span data-ttu-id="4a0d6-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4a0d6-127">NOTES</span></span>

## <span data-ttu-id="4a0d6-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4a0d6-128">RELATED LINKS</span></span>

[<span data-ttu-id="4a0d6-129">Get-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="4a0d6-129">Get-AzureRmBatchApplication</span></span>](./Get-AzureRmBatchApplication.md)

[<span data-ttu-id="4a0d6-130">Get-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="4a0d6-130">Get-AzureRmBatchApplicationPackage</span></span>](./Get-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="4a0d6-131">Nowe — AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="4a0d6-131">New-AzureRmBatchApplication</span></span>](./New-AzureRmBatchApplication.md)

[<span data-ttu-id="4a0d6-132">Nowe — AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="4a0d6-132">New-AzureRmBatchApplicationPackage</span></span>](./New-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="4a0d6-133">Remove-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="4a0d6-133">Remove-AzureRmBatchApplication</span></span>](./Remove-AzureRmBatchApplication.md)

[<span data-ttu-id="4a0d6-134">Set-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="4a0d6-134">Set-AzureRmBatchApplication</span></span>](./Set-AzureRmBatchApplication.md)


