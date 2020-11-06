---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 2B5FC268-4888-4AEB-B125-7263CF2E4DCD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/new-azurermintegrationaccountpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/New-AzureRmIntegrationAccountPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/New-AzureRmIntegrationAccountPartner.md
ms.openlocfilehash: 470a400721d911e09c7bed4e51eb6cef39a1dafa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93548087"
---
# <span data-ttu-id="7ce6d-101">New-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="7ce6d-101">New-AzureRmIntegrationAccountPartner</span></span>

## <span data-ttu-id="7ce6d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7ce6d-102">SYNOPSIS</span></span>
<span data-ttu-id="7ce6d-103">Tworzy partnera kont integracji.</span><span class="sxs-lookup"><span data-stu-id="7ce6d-103">Creates an integration account partner.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7ce6d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7ce6d-104">SYNTAX</span></span>

```
New-AzureRmIntegrationAccountPartner -ResourceGroupName <String> -Name <String> -PartnerName <String>
 [-PartnerType <String>] -BusinessIdentities <Object> [-Metadata <Object>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7ce6d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="7ce6d-105">DESCRIPTION</span></span>
<span data-ttu-id="7ce6d-106">Polecenie cmdlet **New-AzureRmIntegrationAccountPartner** umożliwia utworzenie partnera kont integracji.</span><span class="sxs-lookup"><span data-stu-id="7ce6d-106">The **New-AzureRmIntegrationAccountPartner** cmdlet creates an integration account partner.</span></span>
<span data-ttu-id="7ce6d-107">To polecenie cmdlet zwraca obiekt reprezentujący partnera kont integracji.</span><span class="sxs-lookup"><span data-stu-id="7ce6d-107">This cmdlet returns an object that represents the integration account partner.</span></span>
<span data-ttu-id="7ce6d-108">Określ nazwę konta integracji, nazwę grupy zasobów, nazwę partnera i tożsamości partnerów.</span><span class="sxs-lookup"><span data-stu-id="7ce6d-108">Specify the integration account name, resource group name, partner name, and partner identities.</span></span>

<span data-ttu-id="7ce6d-109">Wartości plików parametrów szablonu określone w wierszu polecenia mają pierwszeństwo przed wartościami parametrów szablonu w obiekcie parametru szablonu.</span><span class="sxs-lookup"><span data-stu-id="7ce6d-109">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>

<span data-ttu-id="7ce6d-110">Ten moduł obsługuje parametry dynamiczne.</span><span class="sxs-lookup"><span data-stu-id="7ce6d-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="7ce6d-111">Aby użyć parametru dynamicznego, wpisz go w poleceniu.</span><span class="sxs-lookup"><span data-stu-id="7ce6d-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="7ce6d-112">Aby wykryć nazwy parametrów dynamicznych, wpisz znak łącznika (-) po nazwie polecenia cmdlet, a następnie naciskaj klawisz Tab, aby przechodzić między dostępnymi parametrami.</span><span class="sxs-lookup"><span data-stu-id="7ce6d-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="7ce6d-113">W przypadku pominięcia wymaganego parametru szablonu polecenie cmdlet monituje o podanie wartości.</span><span class="sxs-lookup"><span data-stu-id="7ce6d-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="7ce6d-114">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7ce6d-114">EXAMPLES</span></span>

### <span data-ttu-id="7ce6d-115">Przykład 1. Tworzenie partnera kont integracji</span><span class="sxs-lookup"><span data-stu-id="7ce6d-115">Example 1: Create an integration account partner</span></span>
```
PS C:\>New-AzureRmIntegrationAccountPartner -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -PartnerName "IntegrationAccountPartner22" -PartnerType "B2B" -BusinessIdentities $BusinessIdentities
Id                 : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/partners/IntegrationAccountPartner1
Name               : IntegrationAccountPartner1
Type               : Microsoft.Logic/integrationAccounts/partners
PartnerType        : B2B
CreatedTime        : 3/26/2016 7:29:30 PM
ChangedTime        : 3/26/2016 7:29:30 PM
BusinessIdentities : [{"Qualifier":"ZZ","Value":"AA"},{"Qualifier":"XX","Value":"GG"}]
Metadata           :
```

<span data-ttu-id="7ce6d-116">To polecenie tworzy partnera kont integracyjnych o nazwie IntegrationAccountPartner22 w określonej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="7ce6d-116">This command creates the integration account partner named IntegrationAccountPartner22 in the specified resource group.</span></span>

## <span data-ttu-id="7ce6d-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7ce6d-117">PARAMETERS</span></span>

### <span data-ttu-id="7ce6d-118">-BusinessIdentities</span><span class="sxs-lookup"><span data-stu-id="7ce6d-118">-BusinessIdentities</span></span>
<span data-ttu-id="7ce6d-119">Określa tożsamość firmową partnera kont integracji.</span><span class="sxs-lookup"><span data-stu-id="7ce6d-119">Specifies business identities for the integration account partner.</span></span>
<span data-ttu-id="7ce6d-120">Określanie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="7ce6d-120">Specify a hash table.</span></span>

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ce6d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ce6d-121">-DefaultProfile</span></span>
<span data-ttu-id="7ce6d-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="7ce6d-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7ce6d-123">-Metadata</span><span class="sxs-lookup"><span data-stu-id="7ce6d-123">-Metadata</span></span>
<span data-ttu-id="7ce6d-124">Określa obiekt metadanych dla partnera.</span><span class="sxs-lookup"><span data-stu-id="7ce6d-124">Specifies a metadata object for the partner.</span></span>

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ce6d-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="7ce6d-125">-Name</span></span>
<span data-ttu-id="7ce6d-126">Określa nazwę konta integracji.</span><span class="sxs-lookup"><span data-stu-id="7ce6d-126">Specifies the name of an integration account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ce6d-127">-Partnername</span><span class="sxs-lookup"><span data-stu-id="7ce6d-127">-PartnerName</span></span>
<span data-ttu-id="7ce6d-128">Określa nazwę partnera kont integracji.</span><span class="sxs-lookup"><span data-stu-id="7ce6d-128">Specifies a name for the integration account partner.</span></span>

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

### <span data-ttu-id="7ce6d-129">-Partnertype</span><span class="sxs-lookup"><span data-stu-id="7ce6d-129">-PartnerType</span></span>
<span data-ttu-id="7ce6d-130">Umożliwia określenie typu konta integracji.</span><span class="sxs-lookup"><span data-stu-id="7ce6d-130">Specifies the type of the integration account.</span></span>
<span data-ttu-id="7ce6d-131">Ten parametr obsługuje typ B2B.</span><span class="sxs-lookup"><span data-stu-id="7ce6d-131">This parameter supports the type B2B.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: B2B

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ce6d-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ce6d-132">-ResourceGroupName</span></span>
<span data-ttu-id="7ce6d-133">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="7ce6d-133">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="7ce6d-134">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7ce6d-134">-Confirm</span></span>
<span data-ttu-id="7ce6d-135">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7ce6d-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ce6d-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7ce6d-136">-WhatIf</span></span>
<span data-ttu-id="7ce6d-137">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7ce6d-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7ce6d-138">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="7ce6d-138">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ce6d-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ce6d-139">CommonParameters</span></span>
<span data-ttu-id="7ce6d-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ce6d-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ce6d-141">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7ce6d-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ce6d-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7ce6d-142">INPUTS</span></span>

### <span data-ttu-id="7ce6d-143">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="7ce6d-143">None</span></span>
<span data-ttu-id="7ce6d-144">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="7ce6d-144">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="7ce6d-145">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7ce6d-145">OUTPUTS</span></span>

### <span data-ttu-id="7ce6d-146">Microsoft. Azure. Management. Logic. MODELES. IntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="7ce6d-146">Microsoft.Azure.Management.Logic.Models.IntegrationAccountPartner</span></span>

## <span data-ttu-id="7ce6d-147">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7ce6d-147">NOTES</span></span>

## <span data-ttu-id="7ce6d-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7ce6d-148">RELATED LINKS</span></span>

[<span data-ttu-id="7ce6d-149">Get-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="7ce6d-149">Get-AzureRmIntegrationAccountPartner</span></span>](./Get-AzureRmIntegrationAccountPartner.md)

[<span data-ttu-id="7ce6d-150">Remove-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="7ce6d-150">Remove-AzureRmIntegrationAccountPartner</span></span>](./Remove-AzureRmIntegrationAccountPartner.md)

[<span data-ttu-id="7ce6d-151">Set-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="7ce6d-151">Set-AzureRmIntegrationAccountPartner</span></span>](./Set-AzureRmIntegrationAccountPartner.md)


