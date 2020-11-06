---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationsecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationSecurityGroup.md
ms.openlocfilehash: 2e39f313e5f6d9c13a9eeb7f4365901ebbea4c9b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93542535"
---
# <span data-ttu-id="727a0-101">Remove-AzureRmApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="727a0-101">Remove-AzureRmApplicationSecurityGroup</span></span>

## <span data-ttu-id="727a0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="727a0-102">SYNOPSIS</span></span>
<span data-ttu-id="727a0-103">Usuwa grupę zabezpieczeń aplikacji.</span><span class="sxs-lookup"><span data-stu-id="727a0-103">Removes an application security group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="727a0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="727a0-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationSecurityGroup -ResourceGroupName <String> -Name <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="727a0-105">Opis</span><span class="sxs-lookup"><span data-stu-id="727a0-105">DESCRIPTION</span></span>
<span data-ttu-id="727a0-106">Polecenie cmdlet **Remove-AzureRmApplicationSecurityGroup** usuwa grupę zabezpieczeń aplikacji.</span><span class="sxs-lookup"><span data-stu-id="727a0-106">The **Remove-AzureRmApplicationSecurityGroup** cmdlet removes an application security group.</span></span>

## <span data-ttu-id="727a0-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="727a0-107">EXAMPLES</span></span>

### <span data-ttu-id="727a0-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="727a0-108">Example 1</span></span>
```
PS C:\>Remove-AzureRmApplicationSecurityGroup -Name "MyApplicationSecurityGrouo" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="727a0-109">To polecenie usuwa grupę zabezpieczeń aplikacji o nazwie MyApplicationSecurityGrouo w grupie zasobów o nazwie Moja zasobów.</span><span class="sxs-lookup"><span data-stu-id="727a0-109">This command deletes an application security group named MyApplicationSecurityGrouo in the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="727a0-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="727a0-110">PARAMETERS</span></span>

### <span data-ttu-id="727a0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="727a0-111">-DefaultProfile</span></span>
<span data-ttu-id="727a0-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="727a0-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="727a0-113">-Force</span><span class="sxs-lookup"><span data-stu-id="727a0-113">-Force</span></span>
<span data-ttu-id="727a0-114">Nie pytaj o potwierdzenie, czy chcesz usunąć zasób</span><span class="sxs-lookup"><span data-stu-id="727a0-114">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="727a0-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="727a0-115">-Name</span></span>
<span data-ttu-id="727a0-116">Nazwa grupy zabezpieczeń aplikacji.</span><span class="sxs-lookup"><span data-stu-id="727a0-116">The name of the application security group.</span></span>

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

### <span data-ttu-id="727a0-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="727a0-117">-PassThru</span></span>
<span data-ttu-id="727a0-118">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="727a0-118">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="727a0-119">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="727a0-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="727a0-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="727a0-120">-ResourceGroupName</span></span>
<span data-ttu-id="727a0-121">Nazwa grupy zasobów grupy zabezpieczeń aplikacji.</span><span class="sxs-lookup"><span data-stu-id="727a0-121">The resource group name of the application security group.</span></span>

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

### <span data-ttu-id="727a0-122">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="727a0-122">-Confirm</span></span>
<span data-ttu-id="727a0-123">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="727a0-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="727a0-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="727a0-124">-WhatIf</span></span>
<span data-ttu-id="727a0-125">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="727a0-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="727a0-126">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="727a0-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="727a0-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="727a0-127">CommonParameters</span></span>
<span data-ttu-id="727a0-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="727a0-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="727a0-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="727a0-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="727a0-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="727a0-130">INPUTS</span></span>

### <span data-ttu-id="727a0-131">System. String</span><span class="sxs-lookup"><span data-stu-id="727a0-131">System.String</span></span>

## <span data-ttu-id="727a0-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="727a0-132">OUTPUTS</span></span>

### <span data-ttu-id="727a0-133">System. Object</span><span class="sxs-lookup"><span data-stu-id="727a0-133">System.Object</span></span>

## <span data-ttu-id="727a0-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="727a0-134">NOTES</span></span>

## <span data-ttu-id="727a0-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="727a0-135">RELATED LINKS</span></span>

[<span data-ttu-id="727a0-136">Nowe — AzureRmApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="727a0-136">New-AzureRmApplicationSecurityGroup</span></span>](./New-AzureRmApplicationSecurityGroup.md)

[<span data-ttu-id="727a0-137">Get-AzureRmApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="727a0-137">Get-AzureRmApplicationSecurityGroup</span></span>](./Get-AzureRmApplicationSecurityGroup.md)
