---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9DBD5ADF-C30E-4D1A-A4CB-4D70C21088F3
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzFirewall.md
ms.openlocfilehash: b46540a614f25a3923301e28cd19d8f1b76af53c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93709132"
---
# <span data-ttu-id="71dd1-101">Remove-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="71dd1-101">Remove-AzFirewall</span></span>

## <span data-ttu-id="71dd1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="71dd1-102">SYNOPSIS</span></span>
<span data-ttu-id="71dd1-103">Usuwanie zapory.</span><span class="sxs-lookup"><span data-stu-id="71dd1-103">Remove a Firewall.</span></span>

## <span data-ttu-id="71dd1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="71dd1-104">SYNTAX</span></span>

```
Remove-AzFirewall -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="71dd1-105">Opis</span><span class="sxs-lookup"><span data-stu-id="71dd1-105">DESCRIPTION</span></span>
<span data-ttu-id="71dd1-106">Polecenie cmdlet **Remove-AzFirewall** usuwa zaporę platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="71dd1-106">The **Remove-AzFirewall** cmdlet removes an Azure Firewall.</span></span>

## <span data-ttu-id="71dd1-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="71dd1-107">EXAMPLES</span></span>

### <span data-ttu-id="71dd1-108">1: Tworzenie i usuwanie zapory</span><span class="sxs-lookup"><span data-stu-id="71dd1-108">1: Create and delete a Firewall</span></span>
```
New-AzFirewall -Name "azFw" -ResourceGroupName "rgName" -Location centralus 

Remove-AzFirewall -Name "azFw" -ResourceGroupName "rgName"
Confirm
Are you sure you want to remove resource 'azFw'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
```

<span data-ttu-id="71dd1-109">W tym przykładzie zostanie utworzona Zapora, a następnie zostanie ona usunięta.</span><span class="sxs-lookup"><span data-stu-id="71dd1-109">This example creates a Firewall and then deletes it.</span></span> <span data-ttu-id="71dd1-110">Aby zapobiec wyświetlaniu monitu podczas usuwania zapory, Użyj flagi-Force.</span><span class="sxs-lookup"><span data-stu-id="71dd1-110">To suppress the prompt when deleting the Firewall, use the -Force flag.</span></span>

### <span data-ttu-id="71dd1-111">2: cofnięcie przydziału zapory, a następnie usunięcie zapory</span><span class="sxs-lookup"><span data-stu-id="71dd1-111">2: Deallocate the Firewall, then delete the Firewall</span></span>
```
$firewall=Get-AzFirewall -ResourceGroupName rgName -Name azFw
$firewall.Deallocate()
Remove-AzFirewall -ResourceGroupName rgName -Name azFw
Confirm
Are you sure you want to remove resource 'azFw'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
```

<span data-ttu-id="71dd1-112">W tym przykładzie jest pobierana Zapora, przydzielana jest Zapora, a następnie usuwana jest Zapora.</span><span class="sxs-lookup"><span data-stu-id="71dd1-112">This example retrieves a Firewall, deallocates the firewall, and then deletes the firewall.</span></span> <span data-ttu-id="71dd1-113">Polecenie deallocate umożliwia usunięcie uruchomionej usługi, ale zachowuje konfigurację zapory.</span><span class="sxs-lookup"><span data-stu-id="71dd1-113">The Deallocate command removes the running service but preserves the firewall's configuration.</span></span> <span data-ttu-id="71dd1-114">Jeśli użytkownik chce ponownie uruchomić usługę, należy wywołać metodę allocate na zaporze.</span><span class="sxs-lookup"><span data-stu-id="71dd1-114">If user wants to start the service again, the Allocate method should be called on the firewall.</span></span>
<span data-ttu-id="71dd1-115">Aby zapobiec wyświetlaniu monitu podczas usuwania zapory, Użyj flagi-Force.</span><span class="sxs-lookup"><span data-stu-id="71dd1-115">To suppress the prompt when deleting the Firewall, use the -Force flag.</span></span>

## <span data-ttu-id="71dd1-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="71dd1-116">PARAMETERS</span></span>

### <span data-ttu-id="71dd1-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="71dd1-117">-AsJob</span></span>
<span data-ttu-id="71dd1-118">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="71dd1-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="71dd1-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71dd1-119">-DefaultProfile</span></span>
<span data-ttu-id="71dd1-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="71dd1-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="71dd1-121">-Force</span><span class="sxs-lookup"><span data-stu-id="71dd1-121">-Force</span></span>
<span data-ttu-id="71dd1-122">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="71dd1-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="71dd1-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="71dd1-123">-Name</span></span>
<span data-ttu-id="71dd1-124">Określa nazwę zapory, która zostanie usunięta przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="71dd1-124">Specifies the name of the firewall that this cmdlet removes.</span></span>

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

### <span data-ttu-id="71dd1-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="71dd1-125">-PassThru</span></span>
<span data-ttu-id="71dd1-126">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="71dd1-126">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="71dd1-127">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="71dd1-127">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="71dd1-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71dd1-128">-ResourceGroupName</span></span>
<span data-ttu-id="71dd1-129">Określa nazwę grupy zasobów zawierającej zaporę, która zostanie usunięta przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="71dd1-129">Specifies the name of the resource group that contains the firewall that this cmdlet removes.</span></span>

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

### <span data-ttu-id="71dd1-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="71dd1-130">-Confirm</span></span>
<span data-ttu-id="71dd1-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="71dd1-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="71dd1-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="71dd1-132">-WhatIf</span></span>
<span data-ttu-id="71dd1-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="71dd1-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="71dd1-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="71dd1-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="71dd1-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71dd1-135">CommonParameters</span></span>
<span data-ttu-id="71dd1-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71dd1-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71dd1-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71dd1-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71dd1-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="71dd1-138">INPUTS</span></span>

### <span data-ttu-id="71dd1-139">System. String</span><span class="sxs-lookup"><span data-stu-id="71dd1-139">System.String</span></span>

## <span data-ttu-id="71dd1-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="71dd1-140">OUTPUTS</span></span>

### <span data-ttu-id="71dd1-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="71dd1-141">System.Boolean</span></span>

## <span data-ttu-id="71dd1-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="71dd1-142">NOTES</span></span>

## <span data-ttu-id="71dd1-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="71dd1-143">RELATED LINKS</span></span>

[<span data-ttu-id="71dd1-144">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="71dd1-144">Get-AzFirewall</span></span>](./Get-AzFirewall.md)

[<span data-ttu-id="71dd1-145">Nowe — AzFirewall</span><span class="sxs-lookup"><span data-stu-id="71dd1-145">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="71dd1-146">Set-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="71dd1-146">Set-AzFirewall</span></span>](./Set-AzFirewall.md)
