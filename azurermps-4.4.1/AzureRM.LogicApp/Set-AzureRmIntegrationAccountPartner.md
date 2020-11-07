---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 9B3B6AD4-C37C-4877-9864-9FB2E3B0BDAB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Set-AzureRmIntegrationAccountPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Set-AzureRmIntegrationAccountPartner.md
ms.openlocfilehash: 13b82cbc7b1f83c441f1211f6ebe7aa1f8c59ea5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718175"
---
# <span data-ttu-id="13878-101">Set-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="13878-101">Set-AzureRmIntegrationAccountPartner</span></span>

## <span data-ttu-id="13878-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="13878-102">SYNOPSIS</span></span>
<span data-ttu-id="13878-103">Modyfikuje partnera kont integracji.</span><span class="sxs-lookup"><span data-stu-id="13878-103">Modifies an integration account partner.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="13878-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="13878-104">SYNTAX</span></span>

```
Set-AzureRmIntegrationAccountPartner -ResourceGroupName <String> -Name <String> -PartnerName <String>
 [-PartnerType <String>] [-BusinessIdentities <Object>] [-Metadata <Object>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="13878-105">Opis</span><span class="sxs-lookup"><span data-stu-id="13878-105">DESCRIPTION</span></span>
<span data-ttu-id="13878-106">Polecenie cmdlet **Set-AzureRmIntegrationAccountPartner** modyfikuje partnera kont integracji.</span><span class="sxs-lookup"><span data-stu-id="13878-106">The **Set-AzureRmIntegrationAccountPartner** cmdlet modifies an integration account partner.</span></span>
<span data-ttu-id="13878-107">To polecenie cmdlet zwraca obiekt reprezentujący partnera kont integracji.</span><span class="sxs-lookup"><span data-stu-id="13878-107">This cmdlet returns an object that represents the integration account partner.</span></span>
<span data-ttu-id="13878-108">Określ nazwę konta integracji, nazwę grupy zasobów i nazwę partnera.</span><span class="sxs-lookup"><span data-stu-id="13878-108">Specify the integration account name, resource group name, and partner name.</span></span>

<span data-ttu-id="13878-109">Ten moduł obsługuje parametry dynamiczne.</span><span class="sxs-lookup"><span data-stu-id="13878-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="13878-110">Aby użyć parametru dynamicznego, wpisz go w poleceniu.</span><span class="sxs-lookup"><span data-stu-id="13878-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="13878-111">Aby wykryć nazwy parametrów dynamicznych, wpisz znak łącznika (-) po nazwie polecenia cmdlet, a następnie naciskaj klawisz Tab, aby przechodzić między dostępnymi parametrami.</span><span class="sxs-lookup"><span data-stu-id="13878-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="13878-112">W przypadku pominięcia wymaganego parametru szablonu polecenie cmdlet monituje o podanie wartości.</span><span class="sxs-lookup"><span data-stu-id="13878-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="13878-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="13878-113">EXAMPLES</span></span>

### <span data-ttu-id="13878-114">Przykład 1: modyfikowanie partnera kont integracji</span><span class="sxs-lookup"><span data-stu-id="13878-114">Example 1: Modify an integration account partner</span></span>
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

<span data-ttu-id="13878-115">To polecenie modyfikuje partnera kont integracyjnych o nazwie IntegrationAccountPartner22 w określonej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="13878-115">This command modify the integration account partner named IntegrationAccountPartner22 in the specified resource group.</span></span>

## <span data-ttu-id="13878-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="13878-116">PARAMETERS</span></span>

### <span data-ttu-id="13878-117">-BusinessIdentities</span><span class="sxs-lookup"><span data-stu-id="13878-117">-BusinessIdentities</span></span>
<span data-ttu-id="13878-118">Określa tożsamość firmową partnera kont integracji.</span><span class="sxs-lookup"><span data-stu-id="13878-118">Specifies business identities for the integration account partner.</span></span>
<span data-ttu-id="13878-119">Określanie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="13878-119">Specify a hash table.</span></span>

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

### <span data-ttu-id="13878-120">-Force</span><span class="sxs-lookup"><span data-stu-id="13878-120">-Force</span></span>
<span data-ttu-id="13878-121">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="13878-121">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="13878-122">-Metadata</span><span class="sxs-lookup"><span data-stu-id="13878-122">-Metadata</span></span>
<span data-ttu-id="13878-123">Określa obiekt metadanych dla partnera.</span><span class="sxs-lookup"><span data-stu-id="13878-123">Specifies a metadata object for the partner.</span></span>

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

### <span data-ttu-id="13878-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="13878-124">-Name</span></span>
<span data-ttu-id="13878-125">Określa nazwę konta integracji.</span><span class="sxs-lookup"><span data-stu-id="13878-125">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="13878-126">-Partnername</span><span class="sxs-lookup"><span data-stu-id="13878-126">-PartnerName</span></span>
<span data-ttu-id="13878-127">Określa nazwę partnera kont integracji.</span><span class="sxs-lookup"><span data-stu-id="13878-127">Specifies the name of the integration account partner.</span></span>

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

### <span data-ttu-id="13878-128">-Partnertype</span><span class="sxs-lookup"><span data-stu-id="13878-128">-PartnerType</span></span>
<span data-ttu-id="13878-129">Umożliwia określenie typu konta integracji.</span><span class="sxs-lookup"><span data-stu-id="13878-129">Specifies the type of the integration account.</span></span>
<span data-ttu-id="13878-130">Ten parametr obsługuje typ B2B.</span><span class="sxs-lookup"><span data-stu-id="13878-130">This parameter supports the type B2B.</span></span>

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

### <span data-ttu-id="13878-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13878-131">-ResourceGroupName</span></span>
<span data-ttu-id="13878-132">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="13878-132">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="13878-133">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="13878-133">-Confirm</span></span>
<span data-ttu-id="13878-134">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="13878-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="13878-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="13878-135">-WhatIf</span></span>
<span data-ttu-id="13878-136">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="13878-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="13878-137">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="13878-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="13878-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13878-138">-DefaultProfile</span></span>
<span data-ttu-id="13878-139">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="13878-139">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="13878-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13878-140">CommonParameters</span></span>
<span data-ttu-id="13878-141">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13878-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13878-142">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="13878-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13878-143">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="13878-143">INPUTS</span></span>

## <span data-ttu-id="13878-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="13878-144">OUTPUTS</span></span>

### <span data-ttu-id="13878-145">Microsoft. Azure. Management. Logic. MODELES. IntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="13878-145">Microsoft.Azure.Management.Logic.Models.IntegrationAccountPartner</span></span>

## <span data-ttu-id="13878-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="13878-146">NOTES</span></span>

## <span data-ttu-id="13878-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="13878-147">RELATED LINKS</span></span>

[<span data-ttu-id="13878-148">Get-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="13878-148">Get-AzureRmIntegrationAccountPartner</span></span>](./Get-AzureRmIntegrationAccountPartner.md)

[<span data-ttu-id="13878-149">Nowe — AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="13878-149">New-AzureRmIntegrationAccountPartner</span></span>](./New-AzureRmIntegrationAccountPartner.md)

[<span data-ttu-id="13878-150">Remove-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="13878-150">Remove-AzureRmIntegrationAccountPartner</span></span>](./Remove-AzureRmIntegrationAccountPartner.md)


