---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationsecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzApplicationSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzApplicationSecurityGroup.md
ms.openlocfilehash: 1bdad35adef15c15c77753c77533f35cfaf945ea
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93890322"
---
# <span data-ttu-id="3650b-101">Remove-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="3650b-101">Remove-AzApplicationSecurityGroup</span></span>

## <span data-ttu-id="3650b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3650b-102">SYNOPSIS</span></span>
<span data-ttu-id="3650b-103">Usuwa grupę zabezpieczeń aplikacji.</span><span class="sxs-lookup"><span data-stu-id="3650b-103">Removes an application security group.</span></span>

## <span data-ttu-id="3650b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3650b-104">SYNTAX</span></span>

```
Remove-AzApplicationSecurityGroup -ResourceGroupName <String> -Name <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3650b-105">Opis</span><span class="sxs-lookup"><span data-stu-id="3650b-105">DESCRIPTION</span></span>
<span data-ttu-id="3650b-106">Polecenie cmdlet **Remove-AzApplicationSecurityGroup** usuwa grupę zabezpieczeń aplikacji.</span><span class="sxs-lookup"><span data-stu-id="3650b-106">The **Remove-AzApplicationSecurityGroup** cmdlet removes an application security group.</span></span>

## <span data-ttu-id="3650b-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3650b-107">EXAMPLES</span></span>

### <span data-ttu-id="3650b-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="3650b-108">Example 1</span></span>
```
PS C:\>Remove-AzApplicationSecurityGroup -Name "MyApplicationSecurityGrouo" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="3650b-109">To polecenie usuwa grupę zabezpieczeń aplikacji o nazwie MyApplicationSecurityGrouo w grupie zasobów o nazwie Moja zasobów.</span><span class="sxs-lookup"><span data-stu-id="3650b-109">This command deletes an application security group named MyApplicationSecurityGrouo in the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="3650b-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3650b-110">PARAMETERS</span></span>

### <span data-ttu-id="3650b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3650b-111">-DefaultProfile</span></span>
<span data-ttu-id="3650b-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3650b-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3650b-113">-Force</span><span class="sxs-lookup"><span data-stu-id="3650b-113">-Force</span></span>
<span data-ttu-id="3650b-114">Nie pytaj o potwierdzenie, czy chcesz usunąć zasób</span><span class="sxs-lookup"><span data-stu-id="3650b-114">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="3650b-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="3650b-115">-Name</span></span>
<span data-ttu-id="3650b-116">Nazwa grupy zabezpieczeń aplikacji.</span><span class="sxs-lookup"><span data-stu-id="3650b-116">The name of the application security group.</span></span>

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

### <span data-ttu-id="3650b-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3650b-117">-PassThru</span></span>
<span data-ttu-id="3650b-118">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="3650b-118">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="3650b-119">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="3650b-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="3650b-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3650b-120">-ResourceGroupName</span></span>
<span data-ttu-id="3650b-121">Nazwa grupy zasobów grupy zabezpieczeń aplikacji.</span><span class="sxs-lookup"><span data-stu-id="3650b-121">The resource group name of the application security group.</span></span>

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

### <span data-ttu-id="3650b-122">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3650b-122">-Confirm</span></span>
<span data-ttu-id="3650b-123">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3650b-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3650b-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3650b-124">-WhatIf</span></span>
<span data-ttu-id="3650b-125">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3650b-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3650b-126">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="3650b-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3650b-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3650b-127">CommonParameters</span></span>
<span data-ttu-id="3650b-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3650b-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3650b-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3650b-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3650b-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3650b-130">INPUTS</span></span>

### <span data-ttu-id="3650b-131">System. String</span><span class="sxs-lookup"><span data-stu-id="3650b-131">System.String</span></span>

## <span data-ttu-id="3650b-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3650b-132">OUTPUTS</span></span>

### <span data-ttu-id="3650b-133">System. Object</span><span class="sxs-lookup"><span data-stu-id="3650b-133">System.Object</span></span>

## <span data-ttu-id="3650b-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3650b-134">NOTES</span></span>

## <span data-ttu-id="3650b-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3650b-135">RELATED LINKS</span></span>

[<span data-ttu-id="3650b-136">Nowe — AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="3650b-136">New-AzApplicationSecurityGroup</span></span>](./New-AzApplicationSecurityGroup.md)

[<span data-ttu-id="3650b-137">Get-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="3650b-137">Get-AzApplicationSecurityGroup</span></span>](./Get-AzApplicationSecurityGroup.md)
