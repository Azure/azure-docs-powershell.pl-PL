---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azimagedatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzImageDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzImageDataDisk.md
ms.openlocfilehash: 3c7399e3eec760e8d4a40d58a8ea9a56e744cfd4
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93893566"
---
# <span data-ttu-id="6175f-101">Remove-AzImageDataDisk</span><span class="sxs-lookup"><span data-stu-id="6175f-101">Remove-AzImageDataDisk</span></span>

## <span data-ttu-id="6175f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6175f-102">SYNOPSIS</span></span>
<span data-ttu-id="6175f-103">Usuwa dysk danych z obiektu obrazu.</span><span class="sxs-lookup"><span data-stu-id="6175f-103">Removes a data disk from an image object.</span></span>

## <span data-ttu-id="6175f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6175f-104">SYNTAX</span></span>

```
Remove-AzImageDataDisk [-Image] <PSImage> [-Lun] <Int32> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6175f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="6175f-105">DESCRIPTION</span></span>
<span data-ttu-id="6175f-106">Polecenie cmdlet **Remove-AzImageDataDisk** usuwa dysk danych z obiektu obrazu.</span><span class="sxs-lookup"><span data-stu-id="6175f-106">The **Remove-AzImageDataDisk** cmdlet removes a data disk from an image object.</span></span>

## <span data-ttu-id="6175f-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6175f-107">EXAMPLES</span></span>

### <span data-ttu-id="6175f-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="6175f-108">Example 1</span></span>
```
PS C:\> Get-AzImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' | Remove-AzImageDataDisk -Lun 1 | Update-AzImage;
```

<span data-ttu-id="6175f-109">To polecenie usuwa dysk danych jednostki logicznej o numerze 1 z istniejącego obrazu "Image01" w grupie zasobów "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="6175f-109">This command removes the data disk of logical unit number 1 from the existing image 'Image01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="6175f-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6175f-110">PARAMETERS</span></span>

### <span data-ttu-id="6175f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6175f-111">-DefaultProfile</span></span>
<span data-ttu-id="6175f-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6175f-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6175f-113">-Image</span><span class="sxs-lookup"><span data-stu-id="6175f-113">-Image</span></span>
<span data-ttu-id="6175f-114">Określa lokalny obiekt obrazu.</span><span class="sxs-lookup"><span data-stu-id="6175f-114">Specifies a local image object.</span></span>

```yaml
Type: PSImage
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6175f-115">-LUN</span><span class="sxs-lookup"><span data-stu-id="6175f-115">-Lun</span></span>
<span data-ttu-id="6175f-116">Określa numer jednostki logicznej (LUN).</span><span class="sxs-lookup"><span data-stu-id="6175f-116">Specifies the logical unit number (LUN).</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6175f-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6175f-117">-Confirm</span></span>
<span data-ttu-id="6175f-118">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6175f-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6175f-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6175f-119">-WhatIf</span></span>
<span data-ttu-id="6175f-120">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6175f-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6175f-121">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="6175f-121">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6175f-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6175f-122">CommonParameters</span></span>
<span data-ttu-id="6175f-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6175f-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6175f-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6175f-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6175f-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6175f-125">INPUTS</span></span>

### <span data-ttu-id="6175f-126">Microsoft. Azure. Management. COMPUTE. models. Image</span><span class="sxs-lookup"><span data-stu-id="6175f-126">Microsoft.Azure.Management.Compute.Models.Image</span></span>
<span data-ttu-id="6175f-127">System. Nullable "1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="6175f-127">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="6175f-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6175f-128">OUTPUTS</span></span>

### <span data-ttu-id="6175f-129">Microsoft. Azure. Management. COMPUTE. models. Image</span><span class="sxs-lookup"><span data-stu-id="6175f-129">Microsoft.Azure.Management.Compute.Models.Image</span></span>

## <span data-ttu-id="6175f-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6175f-130">NOTES</span></span>

## <span data-ttu-id="6175f-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6175f-131">RELATED LINKS</span></span>

