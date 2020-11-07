---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 9B3B6AD4-C37C-4877-9864-9FB2E3B0BDAB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/set-azurermintegrationaccountpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Set-AzureRmIntegrationAccountPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Set-AzureRmIntegrationAccountPartner.md
ms.openlocfilehash: ca7e043d8205800322469a59cea6c17ceb96eff6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718836"
---
# <span data-ttu-id="cd4de-101">Set-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="cd4de-101">Set-AzureRmIntegrationAccountPartner</span></span>

## <span data-ttu-id="cd4de-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="cd4de-102">SYNOPSIS</span></span>
<span data-ttu-id="cd4de-103">Modyfikuje partnera kont integracji.</span><span class="sxs-lookup"><span data-stu-id="cd4de-103">Modifies an integration account partner.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cd4de-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="cd4de-104">SYNTAX</span></span>

```
Set-AzureRmIntegrationAccountPartner -ResourceGroupName <String> -Name <String> -PartnerName <String>
 [-PartnerType <String>] [-BusinessIdentities <Object>] [-Metadata <Object>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cd4de-105">Opis</span><span class="sxs-lookup"><span data-stu-id="cd4de-105">DESCRIPTION</span></span>
<span data-ttu-id="cd4de-106">Polecenie cmdlet **Set-AzureRmIntegrationAccountPartner** modyfikuje partnera kont integracji.</span><span class="sxs-lookup"><span data-stu-id="cd4de-106">The **Set-AzureRmIntegrationAccountPartner** cmdlet modifies an integration account partner.</span></span>
<span data-ttu-id="cd4de-107">To polecenie cmdlet zwraca obiekt reprezentujący partnera kont integracji.</span><span class="sxs-lookup"><span data-stu-id="cd4de-107">This cmdlet returns an object that represents the integration account partner.</span></span>
<span data-ttu-id="cd4de-108">Określ nazwę konta integracji, nazwę grupy zasobów i nazwę partnera.</span><span class="sxs-lookup"><span data-stu-id="cd4de-108">Specify the integration account name, resource group name, and partner name.</span></span>
<span data-ttu-id="cd4de-109">Ten moduł obsługuje parametry dynamiczne.</span><span class="sxs-lookup"><span data-stu-id="cd4de-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="cd4de-110">Aby użyć parametru dynamicznego, wpisz go w poleceniu.</span><span class="sxs-lookup"><span data-stu-id="cd4de-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="cd4de-111">Aby wykryć nazwy parametrów dynamicznych, wpisz znak łącznika (-) po nazwie polecenia cmdlet, a następnie naciskaj klawisz Tab, aby przechodzić między dostępnymi parametrami.</span><span class="sxs-lookup"><span data-stu-id="cd4de-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="cd4de-112">W przypadku pominięcia wymaganego parametru szablonu polecenie cmdlet monituje o podanie wartości.</span><span class="sxs-lookup"><span data-stu-id="cd4de-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="cd4de-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="cd4de-113">EXAMPLES</span></span>

### <span data-ttu-id="cd4de-114">Przykład 1: modyfikowanie partnera kont integracji</span><span class="sxs-lookup"><span data-stu-id="cd4de-114">Example 1: Modify an integration account partner</span></span>
```
PS C:\>Set-AzureRmIntegrationAccountPartner -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -PartnerName "IntegrationAccountPartner22" -PartnerType "B2B" -BusinessIdentities $BusinessIdentities
Id                 : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/partners/IntegrationAccountPartner1
Name               : IntegrationAccountPartner1
Type               : Microsoft.Logic/integrationAccounts/partners
PartnerType        : B2B
CreatedTime        : 3/26/2016 7:29:30 PM
ChangedTime        : 3/26/2016 7:29:30 PM
BusinessIdentities : [{"Qualifier":"ZZ","Value":"AA"},{"Qualifier":"XX","Value":"GG"}]
Metadata
```

<span data-ttu-id="cd4de-115">To polecenie modyfikuje partnera kont integracyjnych o nazwie IntegrationAccountPartner22 w określonej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="cd4de-115">This command modify the integration account partner named IntegrationAccountPartner22 in the specified resource group.</span></span>

## <span data-ttu-id="cd4de-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="cd4de-116">PARAMETERS</span></span>

### <span data-ttu-id="cd4de-117">-BusinessIdentities</span><span class="sxs-lookup"><span data-stu-id="cd4de-117">-BusinessIdentities</span></span>
<span data-ttu-id="cd4de-118">Określa tożsamość firmową partnera kont integracji.</span><span class="sxs-lookup"><span data-stu-id="cd4de-118">Specifies business identities for the integration account partner.</span></span>
<span data-ttu-id="cd4de-119">Określanie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="cd4de-119">Specify a hash table.</span></span>

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

### <span data-ttu-id="cd4de-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd4de-120">-DefaultProfile</span></span>
<span data-ttu-id="cd4de-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="cd4de-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cd4de-122">-Force</span><span class="sxs-lookup"><span data-stu-id="cd4de-122">-Force</span></span>
<span data-ttu-id="cd4de-123">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="cd4de-123">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="cd4de-124">-Metadata</span><span class="sxs-lookup"><span data-stu-id="cd4de-124">-Metadata</span></span>
<span data-ttu-id="cd4de-125">Określa obiekt metadanych dla partnera.</span><span class="sxs-lookup"><span data-stu-id="cd4de-125">Specifies a metadata object for the partner.</span></span>

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

### <span data-ttu-id="cd4de-126">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="cd4de-126">-Name</span></span>
<span data-ttu-id="cd4de-127">Określa nazwę konta integracji.</span><span class="sxs-lookup"><span data-stu-id="cd4de-127">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="cd4de-128">-Partnername</span><span class="sxs-lookup"><span data-stu-id="cd4de-128">-PartnerName</span></span>
<span data-ttu-id="cd4de-129">Określa nazwę partnera kont integracji.</span><span class="sxs-lookup"><span data-stu-id="cd4de-129">Specifies the name of the integration account partner.</span></span>

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

### <span data-ttu-id="cd4de-130">-Partnertype</span><span class="sxs-lookup"><span data-stu-id="cd4de-130">-PartnerType</span></span>
<span data-ttu-id="cd4de-131">Umożliwia określenie typu konta integracji.</span><span class="sxs-lookup"><span data-stu-id="cd4de-131">Specifies the type of the integration account.</span></span>
<span data-ttu-id="cd4de-132">Ten parametr obsługuje typ B2B.</span><span class="sxs-lookup"><span data-stu-id="cd4de-132">This parameter supports the type B2B.</span></span>

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

### <span data-ttu-id="cd4de-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd4de-133">-ResourceGroupName</span></span>
<span data-ttu-id="cd4de-134">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="cd4de-134">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="cd4de-135">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="cd4de-135">-Confirm</span></span>
<span data-ttu-id="cd4de-136">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cd4de-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cd4de-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd4de-137">-WhatIf</span></span>
<span data-ttu-id="cd4de-138">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cd4de-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cd4de-139">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="cd4de-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cd4de-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd4de-140">CommonParameters</span></span>
<span data-ttu-id="cd4de-141">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd4de-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd4de-142">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd4de-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd4de-143">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cd4de-143">INPUTS</span></span>

### <span data-ttu-id="cd4de-144">System. String</span><span class="sxs-lookup"><span data-stu-id="cd4de-144">System.String</span></span>

## <span data-ttu-id="cd4de-145">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="cd4de-145">OUTPUTS</span></span>

### <span data-ttu-id="cd4de-146">Microsoft. Azure. Management. Logic. MODELES. IntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="cd4de-146">Microsoft.Azure.Management.Logic.Models.IntegrationAccountPartner</span></span>

## <span data-ttu-id="cd4de-147">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="cd4de-147">NOTES</span></span>

## <span data-ttu-id="cd4de-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cd4de-148">RELATED LINKS</span></span>

[<span data-ttu-id="cd4de-149">Get-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="cd4de-149">Get-AzureRmIntegrationAccountPartner</span></span>](./Get-AzureRmIntegrationAccountPartner.md)

[<span data-ttu-id="cd4de-150">Nowe — AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="cd4de-150">New-AzureRmIntegrationAccountPartner</span></span>](./New-AzureRmIntegrationAccountPartner.md)

[<span data-ttu-id="cd4de-151">Remove-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="cd4de-151">Remove-AzureRmIntegrationAccountPartner</span></span>](./Remove-AzureRmIntegrationAccountPartner.md)


