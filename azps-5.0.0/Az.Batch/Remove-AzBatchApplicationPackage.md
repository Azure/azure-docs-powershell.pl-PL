---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: FD2E3442-9CEA-4390-BE9C-772C7D6FD1E2
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchapplicationpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchApplicationPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchApplicationPackage.md
ms.openlocfilehash: f88994649281d442f37a2bafa2cf2b4f74e6b86e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94231543"
---
# <span data-ttu-id="c3857-101">Remove-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="c3857-101">Remove-AzBatchApplicationPackage</span></span>

## <span data-ttu-id="c3857-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c3857-102">SYNOPSIS</span></span>
<span data-ttu-id="c3857-103">Usuwa rekord pakietu aplikacji i plik binarny.</span><span class="sxs-lookup"><span data-stu-id="c3857-103">Deletes an application package record and the binary file.</span></span>

## <span data-ttu-id="c3857-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c3857-104">SYNTAX</span></span>

```
Remove-AzBatchApplicationPackage [-AccountName] <String> [-ResourceGroupName] <String>
 [-ApplicationName] <String> [-ApplicationVersion] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c3857-105">Opis</span><span class="sxs-lookup"><span data-stu-id="c3857-105">DESCRIPTION</span></span>
<span data-ttu-id="c3857-106">Polecenie cmdlet **Remove-AzBatchApplicationPackage** usuwa rekord pakietu aplikacji i plik binarny z konta usługi Azure Batch.</span><span class="sxs-lookup"><span data-stu-id="c3857-106">The **Remove-AzBatchApplicationPackage** cmdlet deletes an application package record and the binary file from an Azure Batch account.</span></span>

## <span data-ttu-id="c3857-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c3857-107">EXAMPLES</span></span>

### <span data-ttu-id="c3857-108">Przykład 1: Usuwanie pakietu aplikacji z konta partii</span><span class="sxs-lookup"><span data-stu-id="c3857-108">Example 1: Delete an application package from a Batch account</span></span>
```
PS C:\>Remove-AzBatchApplicationPackage -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationName "litware" -ApplicationVersion "1.0"
```

<span data-ttu-id="c3857-109">To polecenie usuwa wersję 1,0 aplikacji Przykładowa z konta ContosoBatchGroup.</span><span class="sxs-lookup"><span data-stu-id="c3857-109">This command deletes version 1.0 of the Litware application from the ContosoBatchGroup account.</span></span>
<span data-ttu-id="c3857-110">Polecenie usunie zarówno rekord pakietu, jak i obiekt BLOB zawierający plik binarny pakietu.</span><span class="sxs-lookup"><span data-stu-id="c3857-110">The command deletes both the package record and the blob that contain the package binary file.</span></span>

## <span data-ttu-id="c3857-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c3857-111">PARAMETERS</span></span>

### <span data-ttu-id="c3857-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="c3857-112">-AccountName</span></span>
<span data-ttu-id="c3857-113">Określa nazwę konta wsadowego, z którego to polecenie cmdlet usuwa pakiet aplikacji.</span><span class="sxs-lookup"><span data-stu-id="c3857-113">Specifies the name of the Batch account from which this cmdlet deletes an application package.</span></span>

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

### <span data-ttu-id="c3857-114">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="c3857-114">-ApplicationName</span></span>
<span data-ttu-id="c3857-115">Określa nazwę aplikacji.</span><span class="sxs-lookup"><span data-stu-id="c3857-115">Specifies the name of the application.</span></span>

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

### <span data-ttu-id="c3857-116">-ApplicationVersion</span><span class="sxs-lookup"><span data-stu-id="c3857-116">-ApplicationVersion</span></span>
<span data-ttu-id="c3857-117">Określa wersję aplikacji.</span><span class="sxs-lookup"><span data-stu-id="c3857-117">Specifies the version of the application.</span></span>

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

### <span data-ttu-id="c3857-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3857-118">-DefaultProfile</span></span>
<span data-ttu-id="c3857-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c3857-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c3857-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c3857-120">-ResourceGroupName</span></span>
<span data-ttu-id="c3857-121">Określa nazwę grupy zasobów zawierającej konto wsadowe.</span><span class="sxs-lookup"><span data-stu-id="c3857-121">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="c3857-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3857-122">CommonParameters</span></span>
<span data-ttu-id="c3857-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3857-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3857-124">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c3857-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3857-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c3857-125">INPUTS</span></span>

### <span data-ttu-id="c3857-126">System. String</span><span class="sxs-lookup"><span data-stu-id="c3857-126">System.String</span></span>

## <span data-ttu-id="c3857-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c3857-127">OUTPUTS</span></span>

### <span data-ttu-id="c3857-128">System. void</span><span class="sxs-lookup"><span data-stu-id="c3857-128">System.Void</span></span>

## <span data-ttu-id="c3857-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c3857-129">NOTES</span></span>

## <span data-ttu-id="c3857-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c3857-130">RELATED LINKS</span></span>

[<span data-ttu-id="c3857-131">Get-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="c3857-131">Get-AzBatchApplication</span></span>](./Get-AzBatchApplication.md)

[<span data-ttu-id="c3857-132">Get-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="c3857-132">Get-AzBatchApplicationPackage</span></span>](./Get-AzBatchApplicationPackage.md)

[<span data-ttu-id="c3857-133">Nowe — AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="c3857-133">New-AzBatchApplication</span></span>](./New-AzBatchApplication.md)

[<span data-ttu-id="c3857-134">Nowe — AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="c3857-134">New-AzBatchApplicationPackage</span></span>](./New-AzBatchApplicationPackage.md)

[<span data-ttu-id="c3857-135">Remove-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="c3857-135">Remove-AzBatchApplication</span></span>](./Remove-AzBatchApplication.md)

[<span data-ttu-id="c3857-136">Set-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="c3857-136">Set-AzBatchApplication</span></span>](./Set-AzBatchApplication.md)


