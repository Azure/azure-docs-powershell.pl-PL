---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 17653793-3CE1-465F-87F7-20B4B8F56193
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchapplicationpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchApplicationPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchApplicationPackage.md
ms.openlocfilehash: 0cbcc49f4b37b150b783467f45dcc7d4d7e53f2c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93710438"
---
# <span data-ttu-id="81e0b-101">Get-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="81e0b-101">Get-AzBatchApplicationPackage</span></span>

## <span data-ttu-id="81e0b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="81e0b-102">SYNOPSIS</span></span>
<span data-ttu-id="81e0b-103">Pobiera informacje o pakiecie aplikacji na koncie wsadowym.</span><span class="sxs-lookup"><span data-stu-id="81e0b-103">Gets information about an application package in a Batch account.</span></span>

## <span data-ttu-id="81e0b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="81e0b-104">SYNTAX</span></span>

```
Get-AzBatchApplicationPackage [-AccountName] <String> [-ResourceGroupName] <String> [-ApplicationId] <String>
 [-ApplicationVersion] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="81e0b-105">Opis</span><span class="sxs-lookup"><span data-stu-id="81e0b-105">DESCRIPTION</span></span>
<span data-ttu-id="81e0b-106">Polecenie cmdlet **Get-AzBatchApplicationPackage** pobiera informacje o pakiecie aplikacji na koncie usługi Azure Batch.</span><span class="sxs-lookup"><span data-stu-id="81e0b-106">The **Get-AzBatchApplicationPackage** cmdlet gets information about an application package in an Azure Batch account.</span></span>

## <span data-ttu-id="81e0b-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="81e0b-107">EXAMPLES</span></span>

### <span data-ttu-id="81e0b-108">Przykład 1: uzyskiwanie szczegółowych informacji o pakiecie aplikacji na koncie wsadowym</span><span class="sxs-lookup"><span data-stu-id="81e0b-108">Example 1: Get details of an application package in a Batch account</span></span>
```
PS C:\>Get-AzBatchApplicationPackage -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationId "Litware" -ApplicationVersion "1.0"
Format             : zip
State              : Active
Version            : 1.0
LastActivationTime : 13/05/2016 4:03:24 AM
StorageUrl         : https://contosobatch.blob.core.windows.net/app-test
StorageUrlExpiry   : 13/05/2016 8:04:44 AM
Id                 : litware
```

<span data-ttu-id="81e0b-109">To polecenie pobiera szczegóły wersji 1,0 pakietu przykładowa.</span><span class="sxs-lookup"><span data-stu-id="81e0b-109">This command gets the details of version 1.0 of the Litware package.</span></span>

## <span data-ttu-id="81e0b-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="81e0b-110">PARAMETERS</span></span>

### <span data-ttu-id="81e0b-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="81e0b-111">-AccountName</span></span>
<span data-ttu-id="81e0b-112">Określa nazwę konta wsadowego, z którego to polecenie cmdlet pobiera informacje.</span><span class="sxs-lookup"><span data-stu-id="81e0b-112">Specifies the name of the Batch account from which this cmdlet gets information.</span></span>

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

### <span data-ttu-id="81e0b-113">-Identyfikator aplikacji</span><span class="sxs-lookup"><span data-stu-id="81e0b-113">-ApplicationId</span></span>
<span data-ttu-id="81e0b-114">Określa identyfikator aplikacji.</span><span class="sxs-lookup"><span data-stu-id="81e0b-114">Specifies the ID of the application.</span></span>

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

### <span data-ttu-id="81e0b-115">-ApplicationVersion</span><span class="sxs-lookup"><span data-stu-id="81e0b-115">-ApplicationVersion</span></span>
<span data-ttu-id="81e0b-116">Określa wersję aplikacji.</span><span class="sxs-lookup"><span data-stu-id="81e0b-116">Specifies the version of the application.</span></span>

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

### <span data-ttu-id="81e0b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81e0b-117">-DefaultProfile</span></span>
<span data-ttu-id="81e0b-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="81e0b-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="81e0b-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81e0b-119">-ResourceGroupName</span></span>
<span data-ttu-id="81e0b-120">Określa nazwę grupy zasobów zawierającej konto wsadowe.</span><span class="sxs-lookup"><span data-stu-id="81e0b-120">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="81e0b-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81e0b-121">CommonParameters</span></span>
<span data-ttu-id="81e0b-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="81e0b-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81e0b-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="81e0b-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81e0b-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="81e0b-124">INPUTS</span></span>

### <span data-ttu-id="81e0b-125">System. String</span><span class="sxs-lookup"><span data-stu-id="81e0b-125">System.String</span></span>

## <span data-ttu-id="81e0b-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="81e0b-126">OUTPUTS</span></span>

### <span data-ttu-id="81e0b-127">Microsoft.Azure.Commands.Batch. Modele. PSApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="81e0b-127">Microsoft.Azure.Commands.Batch.Models.PSApplicationPackage</span></span>

## <span data-ttu-id="81e0b-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="81e0b-128">NOTES</span></span>

## <span data-ttu-id="81e0b-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="81e0b-129">RELATED LINKS</span></span>

[<span data-ttu-id="81e0b-130">Get-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="81e0b-130">Get-AzBatchApplication</span></span>](./Get-AzBatchApplication.md)

[<span data-ttu-id="81e0b-131">Nowe — AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="81e0b-131">New-AzBatchApplication</span></span>](./New-AzBatchApplication.md)

[<span data-ttu-id="81e0b-132">Nowe — AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="81e0b-132">New-AzBatchApplicationPackage</span></span>](./New-AzBatchApplicationPackage.md)

[<span data-ttu-id="81e0b-133">Remove-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="81e0b-133">Remove-AzBatchApplication</span></span>](./Remove-AzBatchApplication.md)

[<span data-ttu-id="81e0b-134">Remove-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="81e0b-134">Remove-AzBatchApplicationPackage</span></span>](./Remove-AzBatchApplicationPackage.md)

[<span data-ttu-id="81e0b-135">Set-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="81e0b-135">Set-AzBatchApplication</span></span>](./Set-AzBatchApplication.md)


