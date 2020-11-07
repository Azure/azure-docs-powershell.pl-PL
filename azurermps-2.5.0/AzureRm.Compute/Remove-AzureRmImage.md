---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermimage
schema: 2.0.0
ms.openlocfilehash: 5e52e75ea1af799eb2640e38cfa0e053b6b3cc7d
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93898957"
---
# <span data-ttu-id="cfe20-101">Remove-AzureRmImage</span><span class="sxs-lookup"><span data-stu-id="cfe20-101">Remove-AzureRmImage</span></span>

## <span data-ttu-id="cfe20-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="cfe20-102">SYNOPSIS</span></span>
<span data-ttu-id="cfe20-103">Usuwa obraz.</span><span class="sxs-lookup"><span data-stu-id="cfe20-103">Removes an image.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cfe20-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="cfe20-104">SYNTAX</span></span>

```
Remove-AzureRmImage [-ResourceGroupName] <String> [-ImageName] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cfe20-105">Opis</span><span class="sxs-lookup"><span data-stu-id="cfe20-105">DESCRIPTION</span></span>
<span data-ttu-id="cfe20-106">Polecenie cmdlet **Remove-AzureRmImage** usuwa obraz..</span><span class="sxs-lookup"><span data-stu-id="cfe20-106">The **Remove-AzureRmImage** cmdlet removes an image..</span></span>

## <span data-ttu-id="cfe20-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="cfe20-107">EXAMPLES</span></span>

### <span data-ttu-id="cfe20-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="cfe20-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' -Force;
```

<span data-ttu-id="cfe20-109">To polecenie usuwa obraz o nazwie "Image01" w grupie zasobów "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="cfe20-109">This command removes the image named 'Image01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="cfe20-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="cfe20-110">PARAMETERS</span></span>

### <span data-ttu-id="cfe20-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cfe20-111">-AsJob</span></span>
<span data-ttu-id="cfe20-112">Uruchom polecenie cmdlet w tle i zwróć zadanie śledzenia postępu.</span><span class="sxs-lookup"><span data-stu-id="cfe20-112">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cfe20-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cfe20-113">-DefaultProfile</span></span>
<span data-ttu-id="cfe20-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="cfe20-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cfe20-115">-Force</span><span class="sxs-lookup"><span data-stu-id="cfe20-115">-Force</span></span>
<span data-ttu-id="cfe20-116">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="cfe20-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cfe20-117">-ImageName</span><span class="sxs-lookup"><span data-stu-id="cfe20-117">-ImageName</span></span>
<span data-ttu-id="cfe20-118">Określa nazwę obrazu.</span><span class="sxs-lookup"><span data-stu-id="cfe20-118">Specifies the name of an image.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cfe20-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cfe20-119">-ResourceGroupName</span></span>
<span data-ttu-id="cfe20-120">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="cfe20-120">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cfe20-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="cfe20-121">-Confirm</span></span>
<span data-ttu-id="cfe20-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cfe20-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cfe20-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cfe20-123">-WhatIf</span></span>
<span data-ttu-id="cfe20-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cfe20-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cfe20-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="cfe20-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cfe20-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cfe20-126">CommonParameters</span></span>
<span data-ttu-id="cfe20-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cfe20-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cfe20-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cfe20-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cfe20-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cfe20-129">INPUTS</span></span>

### <span data-ttu-id="cfe20-130">System. String</span><span class="sxs-lookup"><span data-stu-id="cfe20-130">System.String</span></span>

## <span data-ttu-id="cfe20-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="cfe20-131">OUTPUTS</span></span>

### <span data-ttu-id="cfe20-132">System. Object</span><span class="sxs-lookup"><span data-stu-id="cfe20-132">System.Object</span></span>

## <span data-ttu-id="cfe20-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="cfe20-133">NOTES</span></span>

## <span data-ttu-id="cfe20-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cfe20-134">RELATED LINKS</span></span>

