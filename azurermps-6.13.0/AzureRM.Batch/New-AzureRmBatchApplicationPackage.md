---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: D53DAEB6-DC4F-473C-A193-A1E2A65326D4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/new-azurermbatchapplicationpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureRmBatchApplicationPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureRmBatchApplicationPackage.md
ms.openlocfilehash: bbe3dbc5a929040bfa10efac952b3500529a075d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524581"
---
# <span data-ttu-id="d353f-101">New-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="d353f-101">New-AzureRmBatchApplicationPackage</span></span>

## <span data-ttu-id="d353f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d353f-102">SYNOPSIS</span></span>
<span data-ttu-id="d353f-103">Tworzy pakiet aplikacji na koncie wsadowym.</span><span class="sxs-lookup"><span data-stu-id="d353f-103">Creates an application package in a Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d353f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d353f-104">SYNTAX</span></span>

### <span data-ttu-id="d353f-105">UploadAndActivate (domyślny)</span><span class="sxs-lookup"><span data-stu-id="d353f-105">UploadAndActivate (Default)</span></span>
```
New-AzureRmBatchApplicationPackage [-AccountName] <String> [-ResourceGroupName] <String>
 [-ApplicationId] <String> [-ApplicationVersion] <String> [-Format] <String> -FilePath <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d353f-106">ActivateOnly</span><span class="sxs-lookup"><span data-stu-id="d353f-106">ActivateOnly</span></span>
```
New-AzureRmBatchApplicationPackage [-AccountName] <String> [-ResourceGroupName] <String>
 [-ApplicationId] <String> [-ApplicationVersion] <String> [-Format] <String> [-ActivateOnly]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d353f-107">Opis</span><span class="sxs-lookup"><span data-stu-id="d353f-107">DESCRIPTION</span></span>
<span data-ttu-id="d353f-108">Polecenie cmdlet **New-AzureRmBatchApplicationPackage** tworzy pakiet aplikacji na koncie Azure Batch.</span><span class="sxs-lookup"><span data-stu-id="d353f-108">The **New-AzureRmBatchApplicationPackage** cmdlet creates an application package in an Azure Batch account.</span></span>

## <span data-ttu-id="d353f-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d353f-109">EXAMPLES</span></span>

### <span data-ttu-id="d353f-110">Przykład 1: Instalowanie pakietu aplikacji na koncie wsadowym</span><span class="sxs-lookup"><span data-stu-id="d353f-110">Example 1: Install an application package into a Batch account</span></span>
```
PS C:\>New-AzureRmBatchApplicationPackage -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationId "Litware" -ApplicationVersion "1.0" -FilePath "litware.1.0.zip" -Format "zip"
```

<span data-ttu-id="d353f-111">To polecenie powoduje utworzenie i aktywowanie wersji 1,0 aplikacji Przykładowa oraz przekazywanie zawartości litware.1.0.zip jako zawartości pakietu aplikacji.</span><span class="sxs-lookup"><span data-stu-id="d353f-111">This command creates and activates version 1.0 of the Litware application, and uploads the contents of litware.1.0.zip as the application package content.</span></span>

## <span data-ttu-id="d353f-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d353f-112">PARAMETERS</span></span>

### <span data-ttu-id="d353f-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="d353f-113">-AccountName</span></span>
<span data-ttu-id="d353f-114">Określa nazwę konta wsadowego, do którego to polecenie cmdlet dodaje pakiet aplikacji.</span><span class="sxs-lookup"><span data-stu-id="d353f-114">Specifies the name of the Batch account to which this cmdlet adds an application package.</span></span>

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

### <span data-ttu-id="d353f-115">-ActivateOnly</span><span class="sxs-lookup"><span data-stu-id="d353f-115">-ActivateOnly</span></span>
<span data-ttu-id="d353f-116">Wskazuje, że to polecenie cmdlet uaktywnia pakiet aplikacji, który został już przekazany.</span><span class="sxs-lookup"><span data-stu-id="d353f-116">Indicates that this cmdlet activates an application package that has already been uploaded.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ActivateOnly
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d353f-117">-Identyfikator aplikacji</span><span class="sxs-lookup"><span data-stu-id="d353f-117">-ApplicationId</span></span>
<span data-ttu-id="d353f-118">Określa identyfikator aplikacji.</span><span class="sxs-lookup"><span data-stu-id="d353f-118">Specifies the ID of the application.</span></span>

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

### <span data-ttu-id="d353f-119">-ApplicationVersion</span><span class="sxs-lookup"><span data-stu-id="d353f-119">-ApplicationVersion</span></span>
<span data-ttu-id="d353f-120">Określa wersję aplikacji.</span><span class="sxs-lookup"><span data-stu-id="d353f-120">Specifies the version of the application.</span></span>

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

### <span data-ttu-id="d353f-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d353f-121">-DefaultProfile</span></span>
<span data-ttu-id="d353f-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d353f-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d353f-123">-FilePath</span><span class="sxs-lookup"><span data-stu-id="d353f-123">-FilePath</span></span>
<span data-ttu-id="d353f-124">Określa plik, który ma zostać przekazany jako plik binarny pakietu aplikacji.</span><span class="sxs-lookup"><span data-stu-id="d353f-124">Specifies the file to be uploaded as the application package binary file.</span></span>

```yaml
Type: System.String
Parameter Sets: UploadAndActivate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d353f-125">-Format</span><span class="sxs-lookup"><span data-stu-id="d353f-125">-Format</span></span>
<span data-ttu-id="d353f-126">Określa format pliku binarnego pakietu aplikacji.</span><span class="sxs-lookup"><span data-stu-id="d353f-126">Specifies the format of the application package binary file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d353f-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d353f-127">-ResourceGroupName</span></span>
<span data-ttu-id="d353f-128">Określa nazwę grupy zasobów zawierającej konto wsadowe.</span><span class="sxs-lookup"><span data-stu-id="d353f-128">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="d353f-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d353f-129">CommonParameters</span></span>
<span data-ttu-id="d353f-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d353f-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d353f-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d353f-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d353f-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d353f-132">INPUTS</span></span>

### <span data-ttu-id="d353f-133">System. String</span><span class="sxs-lookup"><span data-stu-id="d353f-133">System.String</span></span>

### <span data-ttu-id="d353f-134">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="d353f-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="d353f-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d353f-135">OUTPUTS</span></span>

### <span data-ttu-id="d353f-136">Microsoft.Azure.Commands.Batch. Modele. PSApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="d353f-136">Microsoft.Azure.Commands.Batch.Models.PSApplicationPackage</span></span>

## <span data-ttu-id="d353f-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d353f-137">NOTES</span></span>

## <span data-ttu-id="d353f-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d353f-138">RELATED LINKS</span></span>

[<span data-ttu-id="d353f-139">Get-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="d353f-139">Get-AzureRmBatchApplication</span></span>](./Get-AzureRmBatchApplication.md)

[<span data-ttu-id="d353f-140">Get-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="d353f-140">Get-AzureRmBatchApplicationPackage</span></span>](./Get-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="d353f-141">Nowe — AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="d353f-141">New-AzureRmBatchApplication</span></span>](./New-AzureRmBatchApplication.md)

[<span data-ttu-id="d353f-142">Remove-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="d353f-142">Remove-AzureRmBatchApplication</span></span>](./Remove-AzureRmBatchApplication.md)

[<span data-ttu-id="d353f-143">Remove-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="d353f-143">Remove-AzureRmBatchApplicationPackage</span></span>](./Remove-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="d353f-144">Set-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="d353f-144">Set-AzureRmBatchApplication</span></span>](./Set-AzureRmBatchApplication.md)


