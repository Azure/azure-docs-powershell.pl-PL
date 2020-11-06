---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 7320B832-50FD-48AE-9089-445318F3B08A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmAvailabilitySet.md
ms.openlocfilehash: 796000ac20ab887d4abd26039da2a111a19141ad
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93546980"
---
# <span data-ttu-id="7d51b-101">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="7d51b-101">Remove-AzureRmAvailabilitySet</span></span>

## <span data-ttu-id="7d51b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7d51b-102">SYNOPSIS</span></span>
<span data-ttu-id="7d51b-103">Usuwa zestaw dostępności z platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="7d51b-103">Removes an availability set from Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7d51b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7d51b-104">SYNTAX</span></span>

```
Remove-AzureRmAvailabilitySet [-ResourceGroupName] <String> [[-Name] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7d51b-105">Opis</span><span class="sxs-lookup"><span data-stu-id="7d51b-105">DESCRIPTION</span></span>
<span data-ttu-id="7d51b-106">Polecenie cmdlet **Remove-AzureRmAvailabilitySet** umożliwia usunięcie zestawu dostępności z platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="7d51b-106">The **Remove-AzureRmAvailabilitySet** cmdlet removes an availability set from Azure.</span></span>

## <span data-ttu-id="7d51b-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7d51b-107">EXAMPLES</span></span>

### <span data-ttu-id="7d51b-108">Przykład 1: usuwanie zestawu dostępności</span><span class="sxs-lookup"><span data-stu-id="7d51b-108">Example 1: Remove an availability set</span></span>
```
PS C:\> Remove-AzureRmAvailabilitySet -Name "AvailabilitySet03" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="7d51b-109">To polecenie usuwa zestaw dostępności o nazwie AvailablitySet03 w grupie zasobów o nazwie ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="7d51b-109">This command removes an availability set named AvailablitySet03 in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="7d51b-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7d51b-110">PARAMETERS</span></span>

### <span data-ttu-id="7d51b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d51b-111">-DefaultProfile</span></span>
<span data-ttu-id="7d51b-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7d51b-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7d51b-113">-Force</span><span class="sxs-lookup"><span data-stu-id="7d51b-113">-Force</span></span>
<span data-ttu-id="7d51b-114">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="7d51b-114">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d51b-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="7d51b-115">-Name</span></span>
<span data-ttu-id="7d51b-116">Nazwa zestawu dostępności.</span><span class="sxs-lookup"><span data-stu-id="7d51b-116">The availability set name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, AvailabilitySetName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d51b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d51b-117">-ResourceGroupName</span></span>
<span data-ttu-id="7d51b-118">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="7d51b-118">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="7d51b-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7d51b-119">-Confirm</span></span>
<span data-ttu-id="7d51b-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7d51b-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d51b-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7d51b-121">-WhatIf</span></span>
<span data-ttu-id="7d51b-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7d51b-122">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="7d51b-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="7d51b-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d51b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d51b-124">CommonParameters</span></span>
<span data-ttu-id="7d51b-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7d51b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d51b-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7d51b-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d51b-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7d51b-127">INPUTS</span></span>

## <span data-ttu-id="7d51b-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7d51b-128">OUTPUTS</span></span>

## <span data-ttu-id="7d51b-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7d51b-129">NOTES</span></span>

## <span data-ttu-id="7d51b-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7d51b-130">RELATED LINKS</span></span>

[<span data-ttu-id="7d51b-131">Get-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="7d51b-131">Get-AzureRmAvailabilitySet</span></span>](./Get-AzureRmAvailabilitySet.md)

[<span data-ttu-id="7d51b-132">Nowe — AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="7d51b-132">New-AzureRmAvailabilitySet</span></span>](./New-AzureRmAvailabilitySet.md)


