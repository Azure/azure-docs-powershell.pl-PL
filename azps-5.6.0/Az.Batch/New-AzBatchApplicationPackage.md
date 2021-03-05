---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: D53DAEB6-DC4F-473C-A193-A1E2A65326D4
online version: https://docs.microsoft.com/powershell/module/az.batch/new-azbatchapplicationpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchApplicationPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchApplicationPackage.md
ms.openlocfilehash: 766f521f5e963f05e51cd000361675a2f81bbb1e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101960890"
---
# <span data-ttu-id="c4b4d-101">New-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="c4b4d-101">New-AzBatchApplicationPackage</span></span>

## <span data-ttu-id="c4b4d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c4b4d-102">SYNOPSIS</span></span>
<span data-ttu-id="c4b4d-103">Tworzy pakiet aplikacji na koncie wsadowym.</span><span class="sxs-lookup"><span data-stu-id="c4b4d-103">Creates an application package in a Batch account.</span></span>

## <span data-ttu-id="c4b4d-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="c4b4d-104">SYNTAX</span></span>

### <span data-ttu-id="c4b4d-105">UploadAndActivate (domyślne)</span><span class="sxs-lookup"><span data-stu-id="c4b4d-105">UploadAndActivate (Default)</span></span>
```
New-AzBatchApplicationPackage [-AccountName] <String> [-ResourceGroupName] <String> [-ApplicationName] <String>
 [-ApplicationVersion] <String> [-Format] <String> -FilePath <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c4b4d-106">ActivateOnly</span><span class="sxs-lookup"><span data-stu-id="c4b4d-106">ActivateOnly</span></span>
```
New-AzBatchApplicationPackage [-AccountName] <String> [-ResourceGroupName] <String> [-ApplicationName] <String>
 [-ApplicationVersion] <String> [-Format] <String> [-ActivateOnly] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c4b4d-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="c4b4d-107">DESCRIPTION</span></span>
<span data-ttu-id="c4b4d-108">Polecenie **cmdlet New-AzBatchApplicationPackage** tworzy pakiet aplikacji na koncie usługi Azure Batch.</span><span class="sxs-lookup"><span data-stu-id="c4b4d-108">The **New-AzBatchApplicationPackage** cmdlet creates an application package in an Azure Batch account.</span></span>

## <span data-ttu-id="c4b4d-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="c4b4d-109">EXAMPLES</span></span>

### <span data-ttu-id="c4b4d-110">Przykład 1. Instalowanie pakietu aplikacji na koncie wsadowym</span><span class="sxs-lookup"><span data-stu-id="c4b4d-110">Example 1: Install an application package into a Batch account</span></span>
```
PS C:\>New-AzBatchApplicationPackage -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationName "Litware" -ApplicationVersion "1.0" -FilePath "litware.1.0.zip" -Format "zip"
```

<span data-ttu-id="c4b4d-111">To polecenie tworzy i aktywuje wersję 1.0 aplikacji Litware oraz przekaże zawartość litware.1.0.zip jako zawartość pakietu aplikacji.</span><span class="sxs-lookup"><span data-stu-id="c4b4d-111">This command creates and activates version 1.0 of the Litware application, and uploads the contents of litware.1.0.zip as the application package content.</span></span>

## <span data-ttu-id="c4b4d-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c4b4d-112">PARAMETERS</span></span>

### <span data-ttu-id="c4b4d-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="c4b4d-113">-AccountName</span></span>
<span data-ttu-id="c4b4d-114">Określa nazwę konta usługi Batch, do którego to polecenie cmdlet dodaje pakiet aplikacji.</span><span class="sxs-lookup"><span data-stu-id="c4b4d-114">Specifies the name of the Batch account to which this cmdlet adds an application package.</span></span>

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

### <span data-ttu-id="c4b4d-115">- ActivateOnly</span><span class="sxs-lookup"><span data-stu-id="c4b4d-115">-ActivateOnly</span></span>
<span data-ttu-id="c4b4d-116">Wskazuje, że to polecenie cmdlet aktywuje pakiet aplikacji, który został już przekazany.</span><span class="sxs-lookup"><span data-stu-id="c4b4d-116">Indicates that this cmdlet activates an application package that has already been uploaded.</span></span>

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

### <span data-ttu-id="c4b4d-117">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="c4b4d-117">-ApplicationName</span></span>
<span data-ttu-id="c4b4d-118">Określa nazwę aplikacji.</span><span class="sxs-lookup"><span data-stu-id="c4b4d-118">Specifies the name of the application.</span></span>

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

### <span data-ttu-id="c4b4d-119">-ApplicationVersion</span><span class="sxs-lookup"><span data-stu-id="c4b4d-119">-ApplicationVersion</span></span>
<span data-ttu-id="c4b4d-120">Określa wersję aplikacji.</span><span class="sxs-lookup"><span data-stu-id="c4b4d-120">Specifies the version of the application.</span></span>

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

### <span data-ttu-id="c4b4d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4b4d-121">-DefaultProfile</span></span>
<span data-ttu-id="c4b4d-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="c4b4d-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c4b4d-123">- FilePath</span><span class="sxs-lookup"><span data-stu-id="c4b4d-123">-FilePath</span></span>
<span data-ttu-id="c4b4d-124">Określa plik do przesłania jako plik binarny pakietu aplikacji.</span><span class="sxs-lookup"><span data-stu-id="c4b4d-124">Specifies the file to be uploaded as the application package binary file.</span></span>

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

### <span data-ttu-id="c4b4d-125">— Format</span><span class="sxs-lookup"><span data-stu-id="c4b4d-125">-Format</span></span>
<span data-ttu-id="c4b4d-126">Określa format pliku binarnego pakietu aplikacji.</span><span class="sxs-lookup"><span data-stu-id="c4b4d-126">Specifies the format of the application package binary file.</span></span>

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

### <span data-ttu-id="c4b4d-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4b4d-127">-ResourceGroupName</span></span>
<span data-ttu-id="c4b4d-128">Określa nazwę grupy zasobów zawierającej konto Batch.</span><span class="sxs-lookup"><span data-stu-id="c4b4d-128">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="c4b4d-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4b4d-129">CommonParameters</span></span>
<span data-ttu-id="c4b4d-130">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4b4d-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4b4d-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c4b4d-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4b4d-132">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c4b4d-132">INPUTS</span></span>

### <span data-ttu-id="c4b4d-133">System.String</span><span class="sxs-lookup"><span data-stu-id="c4b4d-133">System.String</span></span>

### <span data-ttu-id="c4b4d-134">System.Management.Automation.SwitchParameters</span><span class="sxs-lookup"><span data-stu-id="c4b4d-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="c4b4d-135">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c4b4d-135">OUTPUTS</span></span>

### <span data-ttu-id="c4b4d-136">Microsoft.Azure.Commands.Batch. Models.PSApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="c4b4d-136">Microsoft.Azure.Commands.Batch.Models.PSApplicationPackage</span></span>

## <span data-ttu-id="c4b4d-137">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="c4b4d-137">NOTES</span></span>

## <span data-ttu-id="c4b4d-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c4b4d-138">RELATED LINKS</span></span>

[<span data-ttu-id="c4b4d-139">Get-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="c4b4d-139">Get-AzBatchApplication</span></span>](./Get-AzBatchApplication.md)

[<span data-ttu-id="c4b4d-140">Get-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="c4b4d-140">Get-AzBatchApplicationPackage</span></span>](./Get-AzBatchApplicationPackage.md)

[<span data-ttu-id="c4b4d-141">New-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="c4b4d-141">New-AzBatchApplication</span></span>](./New-AzBatchApplication.md)

[<span data-ttu-id="c4b4d-142">Remove-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="c4b4d-142">Remove-AzBatchApplication</span></span>](./Remove-AzBatchApplication.md)

[<span data-ttu-id="c4b4d-143">Remove-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="c4b4d-143">Remove-AzBatchApplicationPackage</span></span>](./Remove-AzBatchApplicationPackage.md)

[<span data-ttu-id="c4b4d-144">Set-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="c4b4d-144">Set-AzBatchApplication</span></span>](./Set-AzBatchApplication.md)


