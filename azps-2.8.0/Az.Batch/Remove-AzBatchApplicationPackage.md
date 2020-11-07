---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: FD2E3442-9CEA-4390-BE9C-772C7D6FD1E2
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchapplicationpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchApplicationPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchApplicationPackage.md
ms.openlocfilehash: f4b47bb2abab783e4a6995ce57512dbd579e25e4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93706656"
---
# <span data-ttu-id="f77cb-101">Remove-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="f77cb-101">Remove-AzBatchApplicationPackage</span></span>

## <span data-ttu-id="f77cb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f77cb-102">SYNOPSIS</span></span>
<span data-ttu-id="f77cb-103">Usuwa rekord pakietu aplikacji i plik binarny.</span><span class="sxs-lookup"><span data-stu-id="f77cb-103">Deletes an application package record and the binary file.</span></span>

## <span data-ttu-id="f77cb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f77cb-104">SYNTAX</span></span>

```
Remove-AzBatchApplicationPackage [-AccountName] <String> [-ResourceGroupName] <String>
 [-ApplicationId] <String> [-ApplicationVersion] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f77cb-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f77cb-105">DESCRIPTION</span></span>
<span data-ttu-id="f77cb-106">Polecenie cmdlet **Remove-AzBatchApplicationPackage** usuwa rekord pakietu aplikacji i plik binarny z konta usługi Azure Batch.</span><span class="sxs-lookup"><span data-stu-id="f77cb-106">The **Remove-AzBatchApplicationPackage** cmdlet deletes an application package record and the binary file from an Azure Batch account.</span></span>

## <span data-ttu-id="f77cb-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f77cb-107">EXAMPLES</span></span>

### <span data-ttu-id="f77cb-108">Przykład 1: Usuwanie pakietu aplikacji z konta partii</span><span class="sxs-lookup"><span data-stu-id="f77cb-108">Example 1: Delete an application package from a Batch account</span></span>
```
PS C:\>Remove-AzBatchApplicationPackage -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationId "litware" -ApplicationVersion "1.0"
```

<span data-ttu-id="f77cb-109">To polecenie usuwa wersję 1,0 aplikacji Przykładowa z konta ContosoBatchGroup.</span><span class="sxs-lookup"><span data-stu-id="f77cb-109">This command deletes version 1.0 of the Litware application from the ContosoBatchGroup account.</span></span>
<span data-ttu-id="f77cb-110">Polecenie usunie zarówno rekord pakietu, jak i obiekt BLOB zawierający plik binarny pakietu.</span><span class="sxs-lookup"><span data-stu-id="f77cb-110">The command deletes both the package record and the blob that contain the package binary file.</span></span>

## <span data-ttu-id="f77cb-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f77cb-111">PARAMETERS</span></span>

### <span data-ttu-id="f77cb-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="f77cb-112">-AccountName</span></span>
<span data-ttu-id="f77cb-113">Określa nazwę konta wsadowego, z którego to polecenie cmdlet usuwa pakiet aplikacji.</span><span class="sxs-lookup"><span data-stu-id="f77cb-113">Specifies the name of the Batch account from which this cmdlet deletes an application package.</span></span>

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

### <span data-ttu-id="f77cb-114">-Identyfikator aplikacji</span><span class="sxs-lookup"><span data-stu-id="f77cb-114">-ApplicationId</span></span>
<span data-ttu-id="f77cb-115">Określa identyfikator aplikacji.</span><span class="sxs-lookup"><span data-stu-id="f77cb-115">Specifies the ID of the application.</span></span>

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

### <span data-ttu-id="f77cb-116">-ApplicationVersion</span><span class="sxs-lookup"><span data-stu-id="f77cb-116">-ApplicationVersion</span></span>
<span data-ttu-id="f77cb-117">Określa wersję aplikacji.</span><span class="sxs-lookup"><span data-stu-id="f77cb-117">Specifies the version of the application.</span></span>

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

### <span data-ttu-id="f77cb-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f77cb-118">-DefaultProfile</span></span>
<span data-ttu-id="f77cb-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f77cb-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f77cb-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f77cb-120">-ResourceGroupName</span></span>
<span data-ttu-id="f77cb-121">Określa nazwę grupy zasobów zawierającej konto wsadowe.</span><span class="sxs-lookup"><span data-stu-id="f77cb-121">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="f77cb-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f77cb-122">CommonParameters</span></span>
<span data-ttu-id="f77cb-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f77cb-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f77cb-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f77cb-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f77cb-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f77cb-125">INPUTS</span></span>

### <span data-ttu-id="f77cb-126">System. String</span><span class="sxs-lookup"><span data-stu-id="f77cb-126">System.String</span></span>

## <span data-ttu-id="f77cb-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f77cb-127">OUTPUTS</span></span>

### <span data-ttu-id="f77cb-128">System. void</span><span class="sxs-lookup"><span data-stu-id="f77cb-128">System.Void</span></span>

## <span data-ttu-id="f77cb-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f77cb-129">NOTES</span></span>

## <span data-ttu-id="f77cb-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f77cb-130">RELATED LINKS</span></span>

[<span data-ttu-id="f77cb-131">Get-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="f77cb-131">Get-AzBatchApplication</span></span>](./Get-AzBatchApplication.md)

[<span data-ttu-id="f77cb-132">Get-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="f77cb-132">Get-AzBatchApplicationPackage</span></span>](./Get-AzBatchApplicationPackage.md)

[<span data-ttu-id="f77cb-133">Nowe — AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="f77cb-133">New-AzBatchApplication</span></span>](./New-AzBatchApplication.md)

[<span data-ttu-id="f77cb-134">Nowe — AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="f77cb-134">New-AzBatchApplicationPackage</span></span>](./New-AzBatchApplicationPackage.md)

[<span data-ttu-id="f77cb-135">Remove-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="f77cb-135">Remove-AzBatchApplication</span></span>](./Remove-AzBatchApplication.md)

[<span data-ttu-id="f77cb-136">Set-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="f77cb-136">Set-AzBatchApplication</span></span>](./Set-AzBatchApplication.md)


