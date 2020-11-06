---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmImage.md
ms.openlocfilehash: 7d6d130f639265cd2b7e2885f117d2e29899b8c6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553347"
---
# <span data-ttu-id="0f1af-101">Remove-AzureRmImage</span><span class="sxs-lookup"><span data-stu-id="0f1af-101">Remove-AzureRmImage</span></span>

## <span data-ttu-id="0f1af-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0f1af-102">SYNOPSIS</span></span>
<span data-ttu-id="0f1af-103">Usuwa obraz.</span><span class="sxs-lookup"><span data-stu-id="0f1af-103">Removes an image.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0f1af-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0f1af-104">SYNTAX</span></span>

```
Remove-AzureRmImage [-ResourceGroupName] <String> [-ImageName] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0f1af-105">Opis</span><span class="sxs-lookup"><span data-stu-id="0f1af-105">DESCRIPTION</span></span>
<span data-ttu-id="0f1af-106">Polecenie cmdlet **Remove-AzureRmImage** usuwa obraz..</span><span class="sxs-lookup"><span data-stu-id="0f1af-106">The **Remove-AzureRmImage** cmdlet removes an image..</span></span>

## <span data-ttu-id="0f1af-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0f1af-107">EXAMPLES</span></span>

### <span data-ttu-id="0f1af-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="0f1af-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' -Force;
```

<span data-ttu-id="0f1af-109">To polecenie usuwa obraz o nazwie "Image01" w grupie zasobów "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="0f1af-109">This command removes the image named 'Image01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="0f1af-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0f1af-110">PARAMETERS</span></span>

### <span data-ttu-id="0f1af-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f1af-111">-DefaultProfile</span></span>
<span data-ttu-id="0f1af-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0f1af-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0f1af-113">-Force</span><span class="sxs-lookup"><span data-stu-id="0f1af-113">-Force</span></span>
<span data-ttu-id="0f1af-114">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="0f1af-114">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f1af-115">-ImageName</span><span class="sxs-lookup"><span data-stu-id="0f1af-115">-ImageName</span></span>
<span data-ttu-id="0f1af-116">Określa nazwę obrazu.</span><span class="sxs-lookup"><span data-stu-id="0f1af-116">Specifies the name of an image.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f1af-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f1af-117">-ResourceGroupName</span></span>
<span data-ttu-id="0f1af-118">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="0f1af-118">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="0f1af-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0f1af-119">-Confirm</span></span>
<span data-ttu-id="0f1af-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0f1af-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0f1af-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0f1af-121">-WhatIf</span></span>
<span data-ttu-id="0f1af-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0f1af-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0f1af-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="0f1af-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0f1af-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f1af-124">CommonParameters</span></span>
<span data-ttu-id="0f1af-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0f1af-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f1af-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0f1af-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f1af-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0f1af-127">INPUTS</span></span>

### <span data-ttu-id="0f1af-128">System. String</span><span class="sxs-lookup"><span data-stu-id="0f1af-128">System.String</span></span>

## <span data-ttu-id="0f1af-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0f1af-129">OUTPUTS</span></span>

### <span data-ttu-id="0f1af-130">System. Object</span><span class="sxs-lookup"><span data-stu-id="0f1af-130">System.Object</span></span>

## <span data-ttu-id="0f1af-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0f1af-131">NOTES</span></span>

## <span data-ttu-id="0f1af-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0f1af-132">RELATED LINKS</span></span>

