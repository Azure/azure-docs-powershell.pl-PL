---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azimagedatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzImageDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzImageDataDisk.md
ms.openlocfilehash: 837f3955b2a98a3f71283321ed2ad11d68706afd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93868980"
---
# <span data-ttu-id="bf413-101">Remove-AzImageDataDisk</span><span class="sxs-lookup"><span data-stu-id="bf413-101">Remove-AzImageDataDisk</span></span>

## <span data-ttu-id="bf413-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bf413-102">SYNOPSIS</span></span>
<span data-ttu-id="bf413-103">Usuwa dysk danych z obiektu obrazu.</span><span class="sxs-lookup"><span data-stu-id="bf413-103">Removes a data disk from an image object.</span></span>

## <span data-ttu-id="bf413-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bf413-104">SYNTAX</span></span>

```
Remove-AzImageDataDisk [-Image] <PSImage> [-Lun] <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bf413-105">Opis</span><span class="sxs-lookup"><span data-stu-id="bf413-105">DESCRIPTION</span></span>
<span data-ttu-id="bf413-106">Polecenie cmdlet **Remove-AzImageDataDisk** usuwa dysk danych z obiektu obrazu.</span><span class="sxs-lookup"><span data-stu-id="bf413-106">The **Remove-AzImageDataDisk** cmdlet removes a data disk from an image object.</span></span>

## <span data-ttu-id="bf413-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bf413-107">EXAMPLES</span></span>

### <span data-ttu-id="bf413-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="bf413-108">Example 1</span></span>
```
PS C:\> Get-AzImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' | Remove-AzImageDataDisk -Lun 1 | Update-AzImage;
```

<span data-ttu-id="bf413-109">To polecenie usuwa dysk danych jednostki logicznej o numerze 1 z istniejącego obrazu "Image01" w grupie zasobów "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="bf413-109">This command removes the data disk of logical unit number 1 from the existing image 'Image01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="bf413-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bf413-110">PARAMETERS</span></span>

### <span data-ttu-id="bf413-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf413-111">-DefaultProfile</span></span>
<span data-ttu-id="bf413-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="bf413-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bf413-113">-Image</span><span class="sxs-lookup"><span data-stu-id="bf413-113">-Image</span></span>
<span data-ttu-id="bf413-114">Określa lokalny obiekt obrazu.</span><span class="sxs-lookup"><span data-stu-id="bf413-114">Specifies a local image object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSImage
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bf413-115">-LUN</span><span class="sxs-lookup"><span data-stu-id="bf413-115">-Lun</span></span>
<span data-ttu-id="bf413-116">Określa numer jednostki logicznej (LUN).</span><span class="sxs-lookup"><span data-stu-id="bf413-116">Specifies the logical unit number (LUN).</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf413-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="bf413-117">-Confirm</span></span>
<span data-ttu-id="bf413-118">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bf413-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf413-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bf413-119">-WhatIf</span></span>
<span data-ttu-id="bf413-120">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bf413-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bf413-121">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="bf413-121">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf413-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf413-122">CommonParameters</span></span>
<span data-ttu-id="bf413-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bf413-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf413-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bf413-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf413-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bf413-125">INPUTS</span></span>

### <span data-ttu-id="bf413-126">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSImage</span><span class="sxs-lookup"><span data-stu-id="bf413-126">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

### <span data-ttu-id="bf413-127">System. Nullable ' 1 [[System. Int32; system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="bf413-127">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="bf413-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bf413-128">OUTPUTS</span></span>

### <span data-ttu-id="bf413-129">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSImage</span><span class="sxs-lookup"><span data-stu-id="bf413-129">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="bf413-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bf413-130">NOTES</span></span>

## <span data-ttu-id="bf413-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bf413-131">RELATED LINKS</span></span>
