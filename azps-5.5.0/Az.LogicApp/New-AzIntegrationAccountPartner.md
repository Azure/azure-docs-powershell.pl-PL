---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 2B5FC268-4888-4AEB-B125-7263CF2E4DCD
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/new-azintegrationaccountpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountPartner.md
ms.openlocfilehash: bbd64f1e6df016efe0bdd22bb0ae848c79566edf
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100203712"
---
# <span data-ttu-id="420c4-101">New-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="420c4-101">New-AzIntegrationAccountPartner</span></span>

## <span data-ttu-id="420c4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="420c4-102">SYNOPSIS</span></span>
<span data-ttu-id="420c4-103">Tworzy partnera konta integracji.</span><span class="sxs-lookup"><span data-stu-id="420c4-103">Creates an integration account partner.</span></span>

## <span data-ttu-id="420c4-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="420c4-104">SYNTAX</span></span>

```
New-AzIntegrationAccountPartner -ResourceGroupName <String> -Name <String> -PartnerName <String>
 [-PartnerType <String>] -BusinessIdentities <Object> [-Metadata <Object>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="420c4-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="420c4-105">DESCRIPTION</span></span>
<span data-ttu-id="420c4-106">Polecenie **cmdlet New-AzIntegrationAccountPartner** tworzy partnera konta integracji.</span><span class="sxs-lookup"><span data-stu-id="420c4-106">The **New-AzIntegrationAccountPartner** cmdlet creates an integration account partner.</span></span>
<span data-ttu-id="420c4-107">To polecenie cmdlet zwraca obiekt reprezentujący partnera konta integracji.</span><span class="sxs-lookup"><span data-stu-id="420c4-107">This cmdlet returns an object that represents the integration account partner.</span></span>
<span data-ttu-id="420c4-108">Określ nazwę konta integracji, nazwę grupy zasobów, nazwę partnera i tożsamości partnerów.</span><span class="sxs-lookup"><span data-stu-id="420c4-108">Specify the integration account name, resource group name, partner name, and partner identities.</span></span>
<span data-ttu-id="420c4-109">Wartości plików parametrów szablonu określone w wierszu polecenia mają pierwszeństwo przed wartościami parametrów szablonu w obiekcie parametru szablonu.</span><span class="sxs-lookup"><span data-stu-id="420c4-109">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>
<span data-ttu-id="420c4-110">Ten moduł obsługuje parametry dynamiczne.</span><span class="sxs-lookup"><span data-stu-id="420c4-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="420c4-111">Aby użyć parametru dynamicznego, wpisz go w poleceniu.</span><span class="sxs-lookup"><span data-stu-id="420c4-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="420c4-112">Aby wykryć nazwy parametrów dynamicznych, wpisz łącznik (-) po nazwie polecenia cmdlet, a następnie naciskaj klawisz Tab, aby przechodzić przez dostępne parametry.</span><span class="sxs-lookup"><span data-stu-id="420c4-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="420c4-113">Jeśli pominiesz wymagany parametr szablonu, polecenie cmdlet wyświetli monit o wartość.</span><span class="sxs-lookup"><span data-stu-id="420c4-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="420c4-114">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="420c4-114">EXAMPLES</span></span>

### <span data-ttu-id="420c4-115">Przykład 1. Tworzenie partnera konta integracji</span><span class="sxs-lookup"><span data-stu-id="420c4-115">Example 1: Create an integration account partner</span></span>
```
PS C:\>New-AzIntegrationAccountPartner -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -PartnerName "IntegrationAccountPartner22" -PartnerType "B2B" -BusinessIdentities $BusinessIdentities
Id                 : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/partners/IntegrationAccountPartner1
Name               : IntegrationAccountPartner1
Type               : Microsoft.Logic/integrationAccounts/partners
PartnerType        : B2B
CreatedTime        : 3/26/2016 7:29:30 PM
ChangedTime        : 3/26/2016 7:29:30 PM
BusinessIdentities : [{"Qualifier":"ZZ","Value":"AA"},{"Qualifier":"XX","Value":"GG"}]
Metadata           :
```

<span data-ttu-id="420c4-116">To polecenie tworzy w określonej grupie zasobów partnera konta integracji o nazwie IntegrationAccountPartner22.</span><span class="sxs-lookup"><span data-stu-id="420c4-116">This command creates the integration account partner named IntegrationAccountPartner22 in the specified resource group.</span></span>

## <span data-ttu-id="420c4-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="420c4-117">PARAMETERS</span></span>

### <span data-ttu-id="420c4-118">—BusinessIdentities</span><span class="sxs-lookup"><span data-stu-id="420c4-118">-BusinessIdentities</span></span>
<span data-ttu-id="420c4-119">Określa tożsamości biznesowe partnera konta integracji.</span><span class="sxs-lookup"><span data-stu-id="420c4-119">Specifies business identities for the integration account partner.</span></span>
<span data-ttu-id="420c4-120">Określ tabelę skrótu.</span><span class="sxs-lookup"><span data-stu-id="420c4-120">Specify a hash table.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="420c4-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="420c4-121">-DefaultProfile</span></span>
<span data-ttu-id="420c4-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="420c4-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="420c4-123">— Metadane</span><span class="sxs-lookup"><span data-stu-id="420c4-123">-Metadata</span></span>
<span data-ttu-id="420c4-124">Określa obiekt metadanych dla partnera.</span><span class="sxs-lookup"><span data-stu-id="420c4-124">Specifies a metadata object for the partner.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="420c4-125">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="420c4-125">-Name</span></span>
<span data-ttu-id="420c4-126">Określa nazwę konta integracji.</span><span class="sxs-lookup"><span data-stu-id="420c4-126">Specifies the name of an integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="420c4-127">-PartnerName</span><span class="sxs-lookup"><span data-stu-id="420c4-127">-PartnerName</span></span>
<span data-ttu-id="420c4-128">Określa nazwę partnera konta integracji.</span><span class="sxs-lookup"><span data-stu-id="420c4-128">Specifies a name for the integration account partner.</span></span>

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

### <span data-ttu-id="420c4-129">-PartnerType</span><span class="sxs-lookup"><span data-stu-id="420c4-129">-PartnerType</span></span>
<span data-ttu-id="420c4-130">Określa typ konta integracji.</span><span class="sxs-lookup"><span data-stu-id="420c4-130">Specifies the type of the integration account.</span></span>
<span data-ttu-id="420c4-131">Ten parametr obsługuje typ B2B.</span><span class="sxs-lookup"><span data-stu-id="420c4-131">This parameter supports the type B2B.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: B2B

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="420c4-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="420c4-132">-ResourceGroupName</span></span>
<span data-ttu-id="420c4-133">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="420c4-133">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="420c4-134">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="420c4-134">-Confirm</span></span>
<span data-ttu-id="420c4-135">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="420c4-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="420c4-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="420c4-136">-WhatIf</span></span>
<span data-ttu-id="420c4-137">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="420c4-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="420c4-138">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="420c4-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="420c4-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="420c4-139">CommonParameters</span></span>
<span data-ttu-id="420c4-140">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="420c4-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="420c4-141">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="420c4-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="420c4-142">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="420c4-142">INPUTS</span></span>

### <span data-ttu-id="420c4-143">System.String</span><span class="sxs-lookup"><span data-stu-id="420c4-143">System.String</span></span>

## <span data-ttu-id="420c4-144">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="420c4-144">OUTPUTS</span></span>

### <span data-ttu-id="420c4-145">Microsoft.Azure.Management.Logic.Models.IntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="420c4-145">Microsoft.Azure.Management.Logic.Models.IntegrationAccountPartner</span></span>

## <span data-ttu-id="420c4-146">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="420c4-146">NOTES</span></span>

## <span data-ttu-id="420c4-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="420c4-147">RELATED LINKS</span></span>

[<span data-ttu-id="420c4-148">Get-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="420c4-148">Get-AzIntegrationAccountPartner</span></span>](./Get-AzIntegrationAccountPartner.md)

[<span data-ttu-id="420c4-149">Remove-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="420c4-149">Remove-AzIntegrationAccountPartner</span></span>](./Remove-AzIntegrationAccountPartner.md)

[<span data-ttu-id="420c4-150">Set-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="420c4-150">Set-AzIntegrationAccountPartner</span></span>](./Set-AzIntegrationAccountPartner.md)


