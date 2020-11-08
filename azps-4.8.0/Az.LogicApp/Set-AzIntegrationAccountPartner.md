---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 9B3B6AD4-C37C-4877-9864-9FB2E3B0BDAB
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/set-azintegrationaccountpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountPartner.md
ms.openlocfilehash: edd50a72ed0614cf7c71dfbde9f487e8fe632d85
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94064043"
---
# <span data-ttu-id="3db14-101">Set-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="3db14-101">Set-AzIntegrationAccountPartner</span></span>

## <span data-ttu-id="3db14-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3db14-102">SYNOPSIS</span></span>
<span data-ttu-id="3db14-103">Modyfikuje partnera kont integracji.</span><span class="sxs-lookup"><span data-stu-id="3db14-103">Modifies an integration account partner.</span></span>

## <span data-ttu-id="3db14-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3db14-104">SYNTAX</span></span>

```
Set-AzIntegrationAccountPartner -ResourceGroupName <String> -Name <String> -PartnerName <String>
 [-PartnerType <String>] [-BusinessIdentities <Object>] [-Metadata <Object>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3db14-105">Opis</span><span class="sxs-lookup"><span data-stu-id="3db14-105">DESCRIPTION</span></span>
<span data-ttu-id="3db14-106">Polecenie cmdlet **Set-AzIntegrationAccountPartner** modyfikuje partnera kont integracji.</span><span class="sxs-lookup"><span data-stu-id="3db14-106">The **Set-AzIntegrationAccountPartner** cmdlet modifies an integration account partner.</span></span>
<span data-ttu-id="3db14-107">To polecenie cmdlet zwraca obiekt reprezentujący partnera kont integracji.</span><span class="sxs-lookup"><span data-stu-id="3db14-107">This cmdlet returns an object that represents the integration account partner.</span></span>
<span data-ttu-id="3db14-108">Określ nazwę konta integracji, nazwę grupy zasobów i nazwę partnera.</span><span class="sxs-lookup"><span data-stu-id="3db14-108">Specify the integration account name, resource group name, and partner name.</span></span>
<span data-ttu-id="3db14-109">Ten moduł obsługuje parametry dynamiczne.</span><span class="sxs-lookup"><span data-stu-id="3db14-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="3db14-110">Aby użyć parametru dynamicznego, wpisz go w poleceniu.</span><span class="sxs-lookup"><span data-stu-id="3db14-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="3db14-111">Aby wykryć nazwy parametrów dynamicznych, wpisz znak łącznika (-) po nazwie polecenia cmdlet, a następnie naciskaj klawisz Tab, aby przechodzić między dostępnymi parametrami.</span><span class="sxs-lookup"><span data-stu-id="3db14-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="3db14-112">W przypadku pominięcia wymaganego parametru szablonu polecenie cmdlet monituje o podanie wartości.</span><span class="sxs-lookup"><span data-stu-id="3db14-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="3db14-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3db14-113">EXAMPLES</span></span>

### <span data-ttu-id="3db14-114">Przykład 1: modyfikowanie partnera kont integracji</span><span class="sxs-lookup"><span data-stu-id="3db14-114">Example 1: Modify an integration account partner</span></span>
```powershell
PS C:\>Set-AzIntegrationAccountPartner -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -PartnerName "IntegrationAccountPartner22" -PartnerType "B2B" -BusinessIdentities $BusinessIdentities
Id                 : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/partners/IntegrationAccountPartner1
Name               : IntegrationAccountPartner1
Type               : Microsoft.Logic/integrationAccounts/partners
PartnerType        : B2B
CreatedTime        : 3/26/2016 7:29:30 PM
ChangedTime        : 3/26/2016 7:29:30 PM
BusinessIdentities : [{"Qualifier":"ZZ","Value":"AA"},{"Qualifier":"XX","Value":"GG"}]
Metadata
```

<span data-ttu-id="3db14-115">To polecenie modyfikuje partnera kont integracyjnych o nazwie IntegrationAccountPartner22 w określonej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="3db14-115">This command modify the integration account partner named IntegrationAccountPartner22 in the specified resource group.</span></span>

### <span data-ttu-id="3db14-116">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="3db14-116">Example 2</span></span>

<span data-ttu-id="3db14-117">Modyfikuje partnera kont integracji.</span><span class="sxs-lookup"><span data-stu-id="3db14-117">Modifies an integration account partner.</span></span> <span data-ttu-id="3db14-118">(autogenerowana)</span><span class="sxs-lookup"><span data-stu-id="3db14-118">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Set-AzIntegrationAccountPartner -BusinessIdentities <Object> -Metadata <Object> -Name 'IntegrationAccount31' -PartnerName 'IntegrationAccountPartner22' -PartnerType B2B -ResourceGroupName 'ResourceGroup11'
```

## <span data-ttu-id="3db14-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3db14-119">PARAMETERS</span></span>

### <span data-ttu-id="3db14-120">-BusinessIdentities</span><span class="sxs-lookup"><span data-stu-id="3db14-120">-BusinessIdentities</span></span>
<span data-ttu-id="3db14-121">Określa tożsamość firmową partnera kont integracji.</span><span class="sxs-lookup"><span data-stu-id="3db14-121">Specifies business identities for the integration account partner.</span></span>
<span data-ttu-id="3db14-122">Określanie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="3db14-122">Specify a hash table.</span></span>

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

### <span data-ttu-id="3db14-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3db14-123">-DefaultProfile</span></span>
<span data-ttu-id="3db14-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="3db14-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3db14-125">-Force</span><span class="sxs-lookup"><span data-stu-id="3db14-125">-Force</span></span>
<span data-ttu-id="3db14-126">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="3db14-126">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="3db14-127">-Metadata</span><span class="sxs-lookup"><span data-stu-id="3db14-127">-Metadata</span></span>
<span data-ttu-id="3db14-128">Określa obiekt metadanych dla partnera.</span><span class="sxs-lookup"><span data-stu-id="3db14-128">Specifies a metadata object for the partner.</span></span>

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

### <span data-ttu-id="3db14-129">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="3db14-129">-Name</span></span>
<span data-ttu-id="3db14-130">Określa nazwę konta integracji.</span><span class="sxs-lookup"><span data-stu-id="3db14-130">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="3db14-131">-Partnername</span><span class="sxs-lookup"><span data-stu-id="3db14-131">-PartnerName</span></span>
<span data-ttu-id="3db14-132">Określa nazwę partnera kont integracji.</span><span class="sxs-lookup"><span data-stu-id="3db14-132">Specifies the name of the integration account partner.</span></span>

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

### <span data-ttu-id="3db14-133">-Partnertype</span><span class="sxs-lookup"><span data-stu-id="3db14-133">-PartnerType</span></span>
<span data-ttu-id="3db14-134">Umożliwia określenie typu konta integracji.</span><span class="sxs-lookup"><span data-stu-id="3db14-134">Specifies the type of the integration account.</span></span>
<span data-ttu-id="3db14-135">Ten parametr obsługuje typ B2B.</span><span class="sxs-lookup"><span data-stu-id="3db14-135">This parameter supports the type B2B.</span></span>

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

### <span data-ttu-id="3db14-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3db14-136">-ResourceGroupName</span></span>
<span data-ttu-id="3db14-137">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="3db14-137">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="3db14-138">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3db14-138">-Confirm</span></span>
<span data-ttu-id="3db14-139">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3db14-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3db14-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3db14-140">-WhatIf</span></span>
<span data-ttu-id="3db14-141">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3db14-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3db14-142">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="3db14-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3db14-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3db14-143">CommonParameters</span></span>
<span data-ttu-id="3db14-144">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3db14-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3db14-145">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3db14-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3db14-146">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3db14-146">INPUTS</span></span>

### <span data-ttu-id="3db14-147">System. String</span><span class="sxs-lookup"><span data-stu-id="3db14-147">System.String</span></span>

## <span data-ttu-id="3db14-148">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3db14-148">OUTPUTS</span></span>

### <span data-ttu-id="3db14-149">Microsoft. Azure. Management. Logic. MODELES. IntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="3db14-149">Microsoft.Azure.Management.Logic.Models.IntegrationAccountPartner</span></span>

## <span data-ttu-id="3db14-150">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3db14-150">NOTES</span></span>

## <span data-ttu-id="3db14-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3db14-151">RELATED LINKS</span></span>

[<span data-ttu-id="3db14-152">Get-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="3db14-152">Get-AzIntegrationAccountPartner</span></span>](./Get-AzIntegrationAccountPartner.md)

[<span data-ttu-id="3db14-153">Nowe — AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="3db14-153">New-AzIntegrationAccountPartner</span></span>](./New-AzIntegrationAccountPartner.md)

[<span data-ttu-id="3db14-154">Remove-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="3db14-154">Remove-AzIntegrationAccountPartner</span></span>](./Remove-AzIntegrationAccountPartner.md)


