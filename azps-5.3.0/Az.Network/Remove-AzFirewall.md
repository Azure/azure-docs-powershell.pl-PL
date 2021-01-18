---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9DBD5ADF-C30E-4D1A-A4CB-4D70C21088F3
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzFirewall.md
ms.openlocfilehash: 52d2907769ac59a9c71fccef6baf08cc4d13bae8
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98500309"
---
# <span data-ttu-id="05d3b-101">Remove-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="05d3b-101">Remove-AzFirewall</span></span>

## <span data-ttu-id="05d3b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="05d3b-102">SYNOPSIS</span></span>
<span data-ttu-id="05d3b-103">Usuwanie zapory.</span><span class="sxs-lookup"><span data-stu-id="05d3b-103">Remove a Firewall.</span></span>

## <span data-ttu-id="05d3b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="05d3b-104">SYNTAX</span></span>

```
Remove-AzFirewall -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="05d3b-105">Opis</span><span class="sxs-lookup"><span data-stu-id="05d3b-105">DESCRIPTION</span></span>
<span data-ttu-id="05d3b-106">Polecenie cmdlet **Remove-AzFirewall** usuwa zaporę platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="05d3b-106">The **Remove-AzFirewall** cmdlet removes an Azure Firewall.</span></span>

## <span data-ttu-id="05d3b-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="05d3b-107">EXAMPLES</span></span>

### <span data-ttu-id="05d3b-108">Przykład 1: Tworzenie i usuwanie zapory</span><span class="sxs-lookup"><span data-stu-id="05d3b-108">Example 1: Create and delete a Firewall</span></span>
```powershell
New-AzFirewall -Name "azFw" -ResourceGroupName "rgName" -Location centralus 

Remove-AzFirewall -Name "azFw" -ResourceGroupName "rgName"
Confirm
Are you sure you want to remove resource 'azFw'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
```

<span data-ttu-id="05d3b-109">W tym przykładzie zostanie utworzona Zapora, a następnie zostanie ona usunięta.</span><span class="sxs-lookup"><span data-stu-id="05d3b-109">This example creates a Firewall and then deletes it.</span></span> <span data-ttu-id="05d3b-110">Aby zapobiec wyświetlaniu monitu podczas usuwania zapory, Użyj flagi-Force.</span><span class="sxs-lookup"><span data-stu-id="05d3b-110">To suppress the prompt when deleting the Firewall, use the -Force flag.</span></span>

## <span data-ttu-id="05d3b-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="05d3b-111">PARAMETERS</span></span>

### <span data-ttu-id="05d3b-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="05d3b-112">-AsJob</span></span>
<span data-ttu-id="05d3b-113">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="05d3b-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="05d3b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05d3b-114">-DefaultProfile</span></span>
<span data-ttu-id="05d3b-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="05d3b-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="05d3b-116">-Force</span><span class="sxs-lookup"><span data-stu-id="05d3b-116">-Force</span></span>
<span data-ttu-id="05d3b-117">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="05d3b-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="05d3b-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="05d3b-118">-Name</span></span>
<span data-ttu-id="05d3b-119">Określa nazwę zapory, która zostanie usunięta przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="05d3b-119">Specifies the name of the firewall that this cmdlet removes.</span></span>

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

### <span data-ttu-id="05d3b-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="05d3b-120">-PassThru</span></span>
<span data-ttu-id="05d3b-121">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="05d3b-121">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="05d3b-122">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="05d3b-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="05d3b-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05d3b-123">-ResourceGroupName</span></span>
<span data-ttu-id="05d3b-124">Określa nazwę grupy zasobów zawierającej zaporę, która zostanie usunięta przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="05d3b-124">Specifies the name of the resource group that contains the firewall that this cmdlet removes.</span></span>

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

### <span data-ttu-id="05d3b-125">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="05d3b-125">-Confirm</span></span>
<span data-ttu-id="05d3b-126">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="05d3b-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="05d3b-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="05d3b-127">-WhatIf</span></span>
<span data-ttu-id="05d3b-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="05d3b-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="05d3b-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="05d3b-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="05d3b-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05d3b-130">CommonParameters</span></span>
<span data-ttu-id="05d3b-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="05d3b-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05d3b-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="05d3b-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05d3b-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="05d3b-133">INPUTS</span></span>

### <span data-ttu-id="05d3b-134">System. String</span><span class="sxs-lookup"><span data-stu-id="05d3b-134">System.String</span></span>

## <span data-ttu-id="05d3b-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="05d3b-135">OUTPUTS</span></span>

### <span data-ttu-id="05d3b-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="05d3b-136">System.Boolean</span></span>

## <span data-ttu-id="05d3b-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="05d3b-137">NOTES</span></span>

## <span data-ttu-id="05d3b-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="05d3b-138">RELATED LINKS</span></span>

[<span data-ttu-id="05d3b-139">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="05d3b-139">Get-AzFirewall</span></span>](./Get-AzFirewall.md)

[<span data-ttu-id="05d3b-140">Nowe — AzFirewall</span><span class="sxs-lookup"><span data-stu-id="05d3b-140">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="05d3b-141">Set-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="05d3b-141">Set-AzFirewall</span></span>](./Set-AzFirewall.md)
