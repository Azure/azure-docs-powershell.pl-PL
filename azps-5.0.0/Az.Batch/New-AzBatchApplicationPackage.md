---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: D53DAEB6-DC4F-473C-A193-A1E2A65326D4
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/new-azbatchapplicationpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchApplicationPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchApplicationPackage.md
ms.openlocfilehash: fc23c99cabe76834204f2fac1f3c18ae7eea1df0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94233227"
---
# <span data-ttu-id="5cd29-101">New-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="5cd29-101">New-AzBatchApplicationPackage</span></span>

## <span data-ttu-id="5cd29-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5cd29-102">SYNOPSIS</span></span>
<span data-ttu-id="5cd29-103">Tworzy pakiet aplikacji na koncie wsadowym.</span><span class="sxs-lookup"><span data-stu-id="5cd29-103">Creates an application package in a Batch account.</span></span>

## <span data-ttu-id="5cd29-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5cd29-104">SYNTAX</span></span>

### <span data-ttu-id="5cd29-105">UploadAndActivate (domyślny)</span><span class="sxs-lookup"><span data-stu-id="5cd29-105">UploadAndActivate (Default)</span></span>
```
New-AzBatchApplicationPackage [-AccountName] <String> [-ResourceGroupName] <String> [-ApplicationName] <String>
 [-ApplicationVersion] <String> [-Format] <String> -FilePath <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5cd29-106">ActivateOnly</span><span class="sxs-lookup"><span data-stu-id="5cd29-106">ActivateOnly</span></span>
```
New-AzBatchApplicationPackage [-AccountName] <String> [-ResourceGroupName] <String> [-ApplicationName] <String>
 [-ApplicationVersion] <String> [-Format] <String> [-ActivateOnly] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5cd29-107">Opis</span><span class="sxs-lookup"><span data-stu-id="5cd29-107">DESCRIPTION</span></span>
<span data-ttu-id="5cd29-108">Polecenie cmdlet **New-AzBatchApplicationPackage** tworzy pakiet aplikacji na koncie Azure Batch.</span><span class="sxs-lookup"><span data-stu-id="5cd29-108">The **New-AzBatchApplicationPackage** cmdlet creates an application package in an Azure Batch account.</span></span>

## <span data-ttu-id="5cd29-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5cd29-109">EXAMPLES</span></span>

### <span data-ttu-id="5cd29-110">Przykład 1: Instalowanie pakietu aplikacji na koncie wsadowym</span><span class="sxs-lookup"><span data-stu-id="5cd29-110">Example 1: Install an application package into a Batch account</span></span>
```
PS C:\>New-AzBatchApplicationPackage -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationName "Litware" -ApplicationVersion "1.0" -FilePath "litware.1.0.zip" -Format "zip"
```

<span data-ttu-id="5cd29-111">To polecenie powoduje utworzenie i aktywowanie wersji 1,0 aplikacji Przykładowa oraz przekazywanie zawartości litware.1.0.zip jako zawartości pakietu aplikacji.</span><span class="sxs-lookup"><span data-stu-id="5cd29-111">This command creates and activates version 1.0 of the Litware application, and uploads the contents of litware.1.0.zip as the application package content.</span></span>

## <span data-ttu-id="5cd29-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5cd29-112">PARAMETERS</span></span>

### <span data-ttu-id="5cd29-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="5cd29-113">-AccountName</span></span>
<span data-ttu-id="5cd29-114">Określa nazwę konta wsadowego, do którego to polecenie cmdlet dodaje pakiet aplikacji.</span><span class="sxs-lookup"><span data-stu-id="5cd29-114">Specifies the name of the Batch account to which this cmdlet adds an application package.</span></span>

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

### <span data-ttu-id="5cd29-115">-ActivateOnly</span><span class="sxs-lookup"><span data-stu-id="5cd29-115">-ActivateOnly</span></span>
<span data-ttu-id="5cd29-116">Wskazuje, że to polecenie cmdlet uaktywnia pakiet aplikacji, który został już przekazany.</span><span class="sxs-lookup"><span data-stu-id="5cd29-116">Indicates that this cmdlet activates an application package that has already been uploaded.</span></span>

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

### <span data-ttu-id="5cd29-117">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="5cd29-117">-ApplicationName</span></span>
<span data-ttu-id="5cd29-118">Określa nazwę aplikacji.</span><span class="sxs-lookup"><span data-stu-id="5cd29-118">Specifies the name of the application.</span></span>

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

### <span data-ttu-id="5cd29-119">-ApplicationVersion</span><span class="sxs-lookup"><span data-stu-id="5cd29-119">-ApplicationVersion</span></span>
<span data-ttu-id="5cd29-120">Określa wersję aplikacji.</span><span class="sxs-lookup"><span data-stu-id="5cd29-120">Specifies the version of the application.</span></span>

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

### <span data-ttu-id="5cd29-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5cd29-121">-DefaultProfile</span></span>
<span data-ttu-id="5cd29-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5cd29-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5cd29-123">-FilePath</span><span class="sxs-lookup"><span data-stu-id="5cd29-123">-FilePath</span></span>
<span data-ttu-id="5cd29-124">Określa plik, który ma zostać przekazany jako plik binarny pakietu aplikacji.</span><span class="sxs-lookup"><span data-stu-id="5cd29-124">Specifies the file to be uploaded as the application package binary file.</span></span>

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

### <span data-ttu-id="5cd29-125">-Format</span><span class="sxs-lookup"><span data-stu-id="5cd29-125">-Format</span></span>
<span data-ttu-id="5cd29-126">Określa format pliku binarnego pakietu aplikacji.</span><span class="sxs-lookup"><span data-stu-id="5cd29-126">Specifies the format of the application package binary file.</span></span>

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

### <span data-ttu-id="5cd29-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5cd29-127">-ResourceGroupName</span></span>
<span data-ttu-id="5cd29-128">Określa nazwę grupy zasobów zawierającej konto wsadowe.</span><span class="sxs-lookup"><span data-stu-id="5cd29-128">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="5cd29-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5cd29-129">CommonParameters</span></span>
<span data-ttu-id="5cd29-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5cd29-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5cd29-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5cd29-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5cd29-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5cd29-132">INPUTS</span></span>

### <span data-ttu-id="5cd29-133">System. String</span><span class="sxs-lookup"><span data-stu-id="5cd29-133">System.String</span></span>

### <span data-ttu-id="5cd29-134">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="5cd29-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="5cd29-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5cd29-135">OUTPUTS</span></span>

### <span data-ttu-id="5cd29-136">Microsoft.Azure.Commands.Batch. Modele. PSApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="5cd29-136">Microsoft.Azure.Commands.Batch.Models.PSApplicationPackage</span></span>

## <span data-ttu-id="5cd29-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5cd29-137">NOTES</span></span>

## <span data-ttu-id="5cd29-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5cd29-138">RELATED LINKS</span></span>

[<span data-ttu-id="5cd29-139">Get-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="5cd29-139">Get-AzBatchApplication</span></span>](./Get-AzBatchApplication.md)

[<span data-ttu-id="5cd29-140">Get-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="5cd29-140">Get-AzBatchApplicationPackage</span></span>](./Get-AzBatchApplicationPackage.md)

[<span data-ttu-id="5cd29-141">Nowe — AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="5cd29-141">New-AzBatchApplication</span></span>](./New-AzBatchApplication.md)

[<span data-ttu-id="5cd29-142">Remove-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="5cd29-142">Remove-AzBatchApplication</span></span>](./Remove-AzBatchApplication.md)

[<span data-ttu-id="5cd29-143">Remove-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="5cd29-143">Remove-AzBatchApplicationPackage</span></span>](./Remove-AzBatchApplicationPackage.md)

[<span data-ttu-id="5cd29-144">Set-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="5cd29-144">Set-AzBatchApplication</span></span>](./Set-AzBatchApplication.md)


