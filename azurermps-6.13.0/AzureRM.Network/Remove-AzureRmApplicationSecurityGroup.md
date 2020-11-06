---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationsecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationSecurityGroup.md
ms.openlocfilehash: a1d0935e7ca61d5eee3055ad9751fd794e093e8d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526170"
---
# <span data-ttu-id="2d380-101">Remove-AzureRmApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="2d380-101">Remove-AzureRmApplicationSecurityGroup</span></span>

## <span data-ttu-id="2d380-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2d380-102">SYNOPSIS</span></span>
<span data-ttu-id="2d380-103">Usuwa grupę zabezpieczeń aplikacji.</span><span class="sxs-lookup"><span data-stu-id="2d380-103">Removes an application security group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2d380-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2d380-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationSecurityGroup -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2d380-105">Opis</span><span class="sxs-lookup"><span data-stu-id="2d380-105">DESCRIPTION</span></span>
<span data-ttu-id="2d380-106">Polecenie cmdlet **Remove-AzureRmApplicationSecurityGroup** usuwa grupę zabezpieczeń aplikacji.</span><span class="sxs-lookup"><span data-stu-id="2d380-106">The **Remove-AzureRmApplicationSecurityGroup** cmdlet removes an application security group.</span></span>

## <span data-ttu-id="2d380-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2d380-107">EXAMPLES</span></span>

### <span data-ttu-id="2d380-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="2d380-108">Example 1</span></span>
```
PS C:\>Remove-AzureRmApplicationSecurityGroup -Name "MyApplicationSecurityGrouo" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="2d380-109">To polecenie usuwa grupę zabezpieczeń aplikacji o nazwie MyApplicationSecurityGrouo w grupie zasobów o nazwie Moja zasobów.</span><span class="sxs-lookup"><span data-stu-id="2d380-109">This command deletes an application security group named MyApplicationSecurityGrouo in the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="2d380-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2d380-110">PARAMETERS</span></span>

### <span data-ttu-id="2d380-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2d380-111">-AsJob</span></span>
<span data-ttu-id="2d380-112">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="2d380-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2d380-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d380-113">-DefaultProfile</span></span>
<span data-ttu-id="2d380-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2d380-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2d380-115">-Force</span><span class="sxs-lookup"><span data-stu-id="2d380-115">-Force</span></span>
<span data-ttu-id="2d380-116">Nie pytaj o potwierdzenie, czy chcesz usunąć zasób</span><span class="sxs-lookup"><span data-stu-id="2d380-116">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="2d380-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="2d380-117">-Name</span></span>
<span data-ttu-id="2d380-118">Nazwa grupy zabezpieczeń aplikacji.</span><span class="sxs-lookup"><span data-stu-id="2d380-118">The name of the application security group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d380-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2d380-119">-PassThru</span></span>
<span data-ttu-id="2d380-120">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="2d380-120">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="2d380-121">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="2d380-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="2d380-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d380-122">-ResourceGroupName</span></span>
<span data-ttu-id="2d380-123">Nazwa grupy zasobów grupy zabezpieczeń aplikacji.</span><span class="sxs-lookup"><span data-stu-id="2d380-123">The resource group name of the application security group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d380-124">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2d380-124">-Confirm</span></span>
<span data-ttu-id="2d380-125">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2d380-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2d380-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2d380-126">-WhatIf</span></span>
<span data-ttu-id="2d380-127">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2d380-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2d380-128">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="2d380-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2d380-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d380-129">CommonParameters</span></span>
<span data-ttu-id="2d380-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2d380-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d380-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2d380-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d380-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2d380-132">INPUTS</span></span>

### <span data-ttu-id="2d380-133">System. String</span><span class="sxs-lookup"><span data-stu-id="2d380-133">System.String</span></span>

## <span data-ttu-id="2d380-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2d380-134">OUTPUTS</span></span>

### <span data-ttu-id="2d380-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2d380-135">System.Boolean</span></span>

## <span data-ttu-id="2d380-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2d380-136">NOTES</span></span>

## <span data-ttu-id="2d380-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2d380-137">RELATED LINKS</span></span>

[<span data-ttu-id="2d380-138">Nowe — AzureRmApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="2d380-138">New-AzureRmApplicationSecurityGroup</span></span>](./New-AzureRmApplicationSecurityGroup.md)

[<span data-ttu-id="2d380-139">Get-AzureRmApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="2d380-139">Get-AzureRmApplicationSecurityGroup</span></span>](./Get-AzureRmApplicationSecurityGroup.md)
