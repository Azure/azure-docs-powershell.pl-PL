---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationsecuritygroup
schema: 2.0.0
ms.openlocfilehash: 48121e165eea27b57ec36301a657a6778f4c14b7
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93897886"
---
# <span data-ttu-id="7bfef-101">Remove-AzureRmApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="7bfef-101">Remove-AzureRmApplicationSecurityGroup</span></span>

## <span data-ttu-id="7bfef-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7bfef-102">SYNOPSIS</span></span>
<span data-ttu-id="7bfef-103">Usuwa grupę zabezpieczeń aplikacji.</span><span class="sxs-lookup"><span data-stu-id="7bfef-103">Removes an application security group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7bfef-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7bfef-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationSecurityGroup -ResourceGroupName <String> -Name <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7bfef-105">Opis</span><span class="sxs-lookup"><span data-stu-id="7bfef-105">DESCRIPTION</span></span>
<span data-ttu-id="7bfef-106">Polecenie cmdlet **Remove-AzureRmApplicationSecurityGroup** usuwa grupę zabezpieczeń aplikacji.</span><span class="sxs-lookup"><span data-stu-id="7bfef-106">The **Remove-AzureRmApplicationSecurityGroup** cmdlet removes an application security group.</span></span>

## <span data-ttu-id="7bfef-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7bfef-107">EXAMPLES</span></span>

### <span data-ttu-id="7bfef-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="7bfef-108">Example 1</span></span>
```
PS C:\>Remove-AzureRmApplicationSecurityGroup -Name "MyApplicationSecurityGrouo" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="7bfef-109">To polecenie usuwa grupę zabezpieczeń aplikacji o nazwie MyApplicationSecurityGrouo w grupie zasobów o nazwie Moja zasobów.</span><span class="sxs-lookup"><span data-stu-id="7bfef-109">This command deletes an application security group named MyApplicationSecurityGrouo in the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="7bfef-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7bfef-110">PARAMETERS</span></span>

### <span data-ttu-id="7bfef-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7bfef-111">-DefaultProfile</span></span>
<span data-ttu-id="7bfef-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7bfef-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7bfef-113">-Force</span><span class="sxs-lookup"><span data-stu-id="7bfef-113">-Force</span></span>
<span data-ttu-id="7bfef-114">Nie pytaj o potwierdzenie, czy chcesz usunąć zasób</span><span class="sxs-lookup"><span data-stu-id="7bfef-114">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="7bfef-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="7bfef-115">-Name</span></span>
<span data-ttu-id="7bfef-116">Nazwa grupy zabezpieczeń aplikacji.</span><span class="sxs-lookup"><span data-stu-id="7bfef-116">The name of the application security group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7bfef-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7bfef-117">-PassThru</span></span>
<span data-ttu-id="7bfef-118">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="7bfef-118">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="7bfef-119">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="7bfef-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="7bfef-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7bfef-120">-ResourceGroupName</span></span>
<span data-ttu-id="7bfef-121">Nazwa grupy zasobów grupy zabezpieczeń aplikacji.</span><span class="sxs-lookup"><span data-stu-id="7bfef-121">The resource group name of the application security group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7bfef-122">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7bfef-122">-Confirm</span></span>
<span data-ttu-id="7bfef-123">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7bfef-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7bfef-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7bfef-124">-WhatIf</span></span>
<span data-ttu-id="7bfef-125">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7bfef-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7bfef-126">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="7bfef-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7bfef-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7bfef-127">CommonParameters</span></span>
<span data-ttu-id="7bfef-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7bfef-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7bfef-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7bfef-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7bfef-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7bfef-130">INPUTS</span></span>

### <span data-ttu-id="7bfef-131">System. String</span><span class="sxs-lookup"><span data-stu-id="7bfef-131">System.String</span></span>

## <span data-ttu-id="7bfef-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7bfef-132">OUTPUTS</span></span>

### <span data-ttu-id="7bfef-133">System. Object</span><span class="sxs-lookup"><span data-stu-id="7bfef-133">System.Object</span></span>

## <span data-ttu-id="7bfef-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7bfef-134">NOTES</span></span>

## <span data-ttu-id="7bfef-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7bfef-135">RELATED LINKS</span></span>

[<span data-ttu-id="7bfef-136">Nowe — AzureRmApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="7bfef-136">New-AzureRmApplicationSecurityGroup</span></span>](./New-AzureRmApplicationSecurityGroup.md)

[<span data-ttu-id="7bfef-137">Get-AzureRmApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="7bfef-137">Get-AzureRmApplicationSecurityGroup</span></span>](./Get-AzureRmApplicationSecurityGroup.md)
