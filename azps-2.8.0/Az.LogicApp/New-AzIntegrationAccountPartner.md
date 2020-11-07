---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 2B5FC268-4888-4AEB-B125-7263CF2E4DCD
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/new-azintegrationaccountpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountPartner.md
ms.openlocfilehash: fe54643e3425d495a78d6a925f9518d965b77d77
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93705014"
---
# <span data-ttu-id="b93a3-101">New-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="b93a3-101">New-AzIntegrationAccountPartner</span></span>

## <span data-ttu-id="b93a3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b93a3-102">SYNOPSIS</span></span>
<span data-ttu-id="b93a3-103">Tworzy partnera kont integracji.</span><span class="sxs-lookup"><span data-stu-id="b93a3-103">Creates an integration account partner.</span></span>

## <span data-ttu-id="b93a3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b93a3-104">SYNTAX</span></span>

```
New-AzIntegrationAccountPartner -ResourceGroupName <String> -Name <String> -PartnerName <String>
 [-PartnerType <String>] -BusinessIdentities <Object> [-Metadata <Object>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b93a3-105">Opis</span><span class="sxs-lookup"><span data-stu-id="b93a3-105">DESCRIPTION</span></span>
<span data-ttu-id="b93a3-106">Polecenie cmdlet **New-AzIntegrationAccountPartner** umożliwia utworzenie partnera kont integracji.</span><span class="sxs-lookup"><span data-stu-id="b93a3-106">The **New-AzIntegrationAccountPartner** cmdlet creates an integration account partner.</span></span>
<span data-ttu-id="b93a3-107">To polecenie cmdlet zwraca obiekt reprezentujący partnera kont integracji.</span><span class="sxs-lookup"><span data-stu-id="b93a3-107">This cmdlet returns an object that represents the integration account partner.</span></span>
<span data-ttu-id="b93a3-108">Określ nazwę konta integracji, nazwę grupy zasobów, nazwę partnera i tożsamości partnerów.</span><span class="sxs-lookup"><span data-stu-id="b93a3-108">Specify the integration account name, resource group name, partner name, and partner identities.</span></span>
<span data-ttu-id="b93a3-109">Wartości plików parametrów szablonu określone w wierszu polecenia mają pierwszeństwo przed wartościami parametrów szablonu w obiekcie parametru szablonu.</span><span class="sxs-lookup"><span data-stu-id="b93a3-109">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>
<span data-ttu-id="b93a3-110">Ten moduł obsługuje parametry dynamiczne.</span><span class="sxs-lookup"><span data-stu-id="b93a3-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="b93a3-111">Aby użyć parametru dynamicznego, wpisz go w poleceniu.</span><span class="sxs-lookup"><span data-stu-id="b93a3-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="b93a3-112">Aby wykryć nazwy parametrów dynamicznych, wpisz znak łącznika (-) po nazwie polecenia cmdlet, a następnie naciskaj klawisz Tab, aby przechodzić między dostępnymi parametrami.</span><span class="sxs-lookup"><span data-stu-id="b93a3-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="b93a3-113">W przypadku pominięcia wymaganego parametru szablonu polecenie cmdlet monituje o podanie wartości.</span><span class="sxs-lookup"><span data-stu-id="b93a3-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="b93a3-114">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b93a3-114">EXAMPLES</span></span>

### <span data-ttu-id="b93a3-115">Przykład 1. Tworzenie partnera kont integracji</span><span class="sxs-lookup"><span data-stu-id="b93a3-115">Example 1: Create an integration account partner</span></span>
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

<span data-ttu-id="b93a3-116">To polecenie tworzy partnera kont integracyjnych o nazwie IntegrationAccountPartner22 w określonej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="b93a3-116">This command creates the integration account partner named IntegrationAccountPartner22 in the specified resource group.</span></span>

## <span data-ttu-id="b93a3-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b93a3-117">PARAMETERS</span></span>

### <span data-ttu-id="b93a3-118">-BusinessIdentities</span><span class="sxs-lookup"><span data-stu-id="b93a3-118">-BusinessIdentities</span></span>
<span data-ttu-id="b93a3-119">Określa tożsamość firmową partnera kont integracji.</span><span class="sxs-lookup"><span data-stu-id="b93a3-119">Specifies business identities for the integration account partner.</span></span>
<span data-ttu-id="b93a3-120">Określanie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="b93a3-120">Specify a hash table.</span></span>

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

### <span data-ttu-id="b93a3-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b93a3-121">-DefaultProfile</span></span>
<span data-ttu-id="b93a3-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="b93a3-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b93a3-123">-Metadata</span><span class="sxs-lookup"><span data-stu-id="b93a3-123">-Metadata</span></span>
<span data-ttu-id="b93a3-124">Określa obiekt metadanych dla partnera.</span><span class="sxs-lookup"><span data-stu-id="b93a3-124">Specifies a metadata object for the partner.</span></span>

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

### <span data-ttu-id="b93a3-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b93a3-125">-Name</span></span>
<span data-ttu-id="b93a3-126">Określa nazwę konta integracji.</span><span class="sxs-lookup"><span data-stu-id="b93a3-126">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="b93a3-127">-Partnername</span><span class="sxs-lookup"><span data-stu-id="b93a3-127">-PartnerName</span></span>
<span data-ttu-id="b93a3-128">Określa nazwę partnera kont integracji.</span><span class="sxs-lookup"><span data-stu-id="b93a3-128">Specifies a name for the integration account partner.</span></span>

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

### <span data-ttu-id="b93a3-129">-Partnertype</span><span class="sxs-lookup"><span data-stu-id="b93a3-129">-PartnerType</span></span>
<span data-ttu-id="b93a3-130">Umożliwia określenie typu konta integracji.</span><span class="sxs-lookup"><span data-stu-id="b93a3-130">Specifies the type of the integration account.</span></span>
<span data-ttu-id="b93a3-131">Ten parametr obsługuje typ B2B.</span><span class="sxs-lookup"><span data-stu-id="b93a3-131">This parameter supports the type B2B.</span></span>

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

### <span data-ttu-id="b93a3-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b93a3-132">-ResourceGroupName</span></span>
<span data-ttu-id="b93a3-133">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b93a3-133">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="b93a3-134">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b93a3-134">-Confirm</span></span>
<span data-ttu-id="b93a3-135">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b93a3-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b93a3-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b93a3-136">-WhatIf</span></span>
<span data-ttu-id="b93a3-137">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b93a3-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b93a3-138">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b93a3-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b93a3-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b93a3-139">CommonParameters</span></span>
<span data-ttu-id="b93a3-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b93a3-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b93a3-141">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b93a3-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b93a3-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b93a3-142">INPUTS</span></span>

### <span data-ttu-id="b93a3-143">System. String</span><span class="sxs-lookup"><span data-stu-id="b93a3-143">System.String</span></span>

## <span data-ttu-id="b93a3-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b93a3-144">OUTPUTS</span></span>

### <span data-ttu-id="b93a3-145">Microsoft. Azure. Management. Logic. MODELES. IntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="b93a3-145">Microsoft.Azure.Management.Logic.Models.IntegrationAccountPartner</span></span>

## <span data-ttu-id="b93a3-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b93a3-146">NOTES</span></span>

## <span data-ttu-id="b93a3-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b93a3-147">RELATED LINKS</span></span>

[<span data-ttu-id="b93a3-148">Get-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="b93a3-148">Get-AzIntegrationAccountPartner</span></span>](./Get-AzIntegrationAccountPartner.md)

[<span data-ttu-id="b93a3-149">Remove-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="b93a3-149">Remove-AzIntegrationAccountPartner</span></span>](./Remove-AzIntegrationAccountPartner.md)

[<span data-ttu-id="b93a3-150">Set-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="b93a3-150">Set-AzIntegrationAccountPartner</span></span>](./Set-AzIntegrationAccountPartner.md)

