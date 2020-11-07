---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: E8A557EA-FE3F-4433-BFDE-B4D73DF8467C
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/remove-azintegrationaccountpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountPartner.md
ms.openlocfilehash: d630a88134b2910a38b21ff964db9748db5cbeeb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93704996"
---
# <span data-ttu-id="c820d-101">Remove-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="c820d-101">Remove-AzIntegrationAccountPartner</span></span>

## <span data-ttu-id="c820d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c820d-102">SYNOPSIS</span></span>
<span data-ttu-id="c820d-103">Usuwa partnera kont integracji.</span><span class="sxs-lookup"><span data-stu-id="c820d-103">Removes an integration account partner.</span></span>

## <span data-ttu-id="c820d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c820d-104">SYNTAX</span></span>

```
Remove-AzIntegrationAccountPartner -ResourceGroupName <String> -Name <String> -PartnerName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c820d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="c820d-105">DESCRIPTION</span></span>
<span data-ttu-id="c820d-106">Polecenie cmdlet **Remove-AzIntegrationAccountPartner** umożliwia usunięcie partnera konta integracji z grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="c820d-106">The **Remove-AzIntegrationAccountPartner** cmdlet removes an integration account partner from a resource group.</span></span>
<span data-ttu-id="c820d-107">Określ nazwę konta integracji, nazwę grupy zasobów i nazwę partnera.</span><span class="sxs-lookup"><span data-stu-id="c820d-107">Specify the integration account name, resource group name, and partner name.</span></span>
<span data-ttu-id="c820d-108">Ten moduł obsługuje parametry dynamiczne.</span><span class="sxs-lookup"><span data-stu-id="c820d-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="c820d-109">Aby użyć parametru dynamicznego, wpisz go w poleceniu.</span><span class="sxs-lookup"><span data-stu-id="c820d-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="c820d-110">Aby wykryć nazwy parametrów dynamicznych, wpisz znak łącznika (-) po nazwie polecenia cmdlet, a następnie naciskaj klawisz Tab, aby przechodzić między dostępnymi parametrami.</span><span class="sxs-lookup"><span data-stu-id="c820d-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="c820d-111">W przypadku pominięcia wymaganego parametru szablonu polecenie cmdlet monituje o podanie wartości.</span><span class="sxs-lookup"><span data-stu-id="c820d-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="c820d-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c820d-112">EXAMPLES</span></span>

### <span data-ttu-id="c820d-113">Przykład 1: usuwanie partnera kont integracji</span><span class="sxs-lookup"><span data-stu-id="c820d-113">Example 1: Remove an integration account partner</span></span>
```
PS C:\>Remove-AzIntegrationAccountPartner -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -PartnerName "IntegrationAccountPartner1"
```

<span data-ttu-id="c820d-114">To polecenie usuwa partnera kont integracyjnych o nazwie IntegrationAccountPartner1.</span><span class="sxs-lookup"><span data-stu-id="c820d-114">This command removes the integration account partner named IntegrationAccountPartner1.</span></span>

## <span data-ttu-id="c820d-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c820d-115">PARAMETERS</span></span>

### <span data-ttu-id="c820d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c820d-116">-DefaultProfile</span></span>
<span data-ttu-id="c820d-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="c820d-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c820d-118">-Force</span><span class="sxs-lookup"><span data-stu-id="c820d-118">-Force</span></span>
<span data-ttu-id="c820d-119">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="c820d-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c820d-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c820d-120">-Name</span></span>
<span data-ttu-id="c820d-121">Określa nazwę konta integracji.</span><span class="sxs-lookup"><span data-stu-id="c820d-121">Specifies the name of an integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c820d-122">-Partnername</span><span class="sxs-lookup"><span data-stu-id="c820d-122">-PartnerName</span></span>
<span data-ttu-id="c820d-123">Określa nazwę partnera kont integracji.</span><span class="sxs-lookup"><span data-stu-id="c820d-123">Specifies the name of the integration account partner.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c820d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c820d-124">-ResourceGroupName</span></span>
<span data-ttu-id="c820d-125">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="c820d-125">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="c820d-126">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c820d-126">-Confirm</span></span>
<span data-ttu-id="c820d-127">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c820d-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c820d-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c820d-128">-WhatIf</span></span>
<span data-ttu-id="c820d-129">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c820d-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c820d-130">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="c820d-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c820d-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c820d-131">CommonParameters</span></span>
<span data-ttu-id="c820d-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c820d-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c820d-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c820d-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c820d-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c820d-134">INPUTS</span></span>

### <span data-ttu-id="c820d-135">System. String</span><span class="sxs-lookup"><span data-stu-id="c820d-135">System.String</span></span>

## <span data-ttu-id="c820d-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c820d-136">OUTPUTS</span></span>

### <span data-ttu-id="c820d-137">System. void</span><span class="sxs-lookup"><span data-stu-id="c820d-137">System.Void</span></span>

## <span data-ttu-id="c820d-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c820d-138">NOTES</span></span>

## <span data-ttu-id="c820d-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c820d-139">RELATED LINKS</span></span>

[<span data-ttu-id="c820d-140">Get-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="c820d-140">Get-AzIntegrationAccountPartner</span></span>](./Get-AzIntegrationAccountPartner.md)

[<span data-ttu-id="c820d-141">Nowe — AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="c820d-141">New-AzIntegrationAccountPartner</span></span>](./New-AzIntegrationAccountPartner.md)

[<span data-ttu-id="c820d-142">Set-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="c820d-142">Set-AzIntegrationAccountPartner</span></span>](./Set-AzIntegrationAccountPartner.md)


