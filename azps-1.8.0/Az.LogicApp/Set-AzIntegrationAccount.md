---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: F6D9EA59-BA61-4117-8771-9B190424BFF8
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/set-azintegrationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccount.md
ms.openlocfilehash: 8c4c97b1574777a05560f7faa64f0bb4a3476bb9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93867620"
---
# <span data-ttu-id="0a049-101">Set-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="0a049-101">Set-AzIntegrationAccount</span></span>

## <span data-ttu-id="0a049-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0a049-102">SYNOPSIS</span></span>
<span data-ttu-id="0a049-103">Modyfikuje konto integracyjne.</span><span class="sxs-lookup"><span data-stu-id="0a049-103">Modifies an integration account.</span></span>

## <span data-ttu-id="0a049-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0a049-104">SYNTAX</span></span>

```
Set-AzIntegrationAccount -ResourceGroupName <String> -Name <String> [-Location <String>] [-Sku <String>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0a049-105">Opis</span><span class="sxs-lookup"><span data-stu-id="0a049-105">DESCRIPTION</span></span>
<span data-ttu-id="0a049-106">Polecenie cmdlet **Set-AzIntegrationAccount** modyfikuje konto integracji.</span><span class="sxs-lookup"><span data-stu-id="0a049-106">The **Set-AzIntegrationAccount** cmdlet modifies an integration account.</span></span>
<span data-ttu-id="0a049-107">To polecenie cmdlet zwraca obiekt reprezentujący konto integracji.</span><span class="sxs-lookup"><span data-stu-id="0a049-107">This cmdlet returns an object that represents the integration account.</span></span>
<span data-ttu-id="0a049-108">Ten moduł obsługuje parametry dynamiczne.</span><span class="sxs-lookup"><span data-stu-id="0a049-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="0a049-109">Aby użyć parametru dynamicznego, wpisz go w poleceniu.</span><span class="sxs-lookup"><span data-stu-id="0a049-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="0a049-110">Aby wykryć nazwy parametrów dynamicznych, wpisz znak łącznika (-) po nazwie polecenia cmdlet, a następnie naciskaj klawisz Tab, aby przechodzić między dostępnymi parametrami.</span><span class="sxs-lookup"><span data-stu-id="0a049-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="0a049-111">W przypadku pominięcia wymaganego parametru szablonu polecenie cmdlet monituje o podanie wartości.</span><span class="sxs-lookup"><span data-stu-id="0a049-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="0a049-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0a049-112">EXAMPLES</span></span>

### <span data-ttu-id="0a049-113">Przykład 1: modyfikowanie konta integracji</span><span class="sxs-lookup"><span data-stu-id="0a049-113">Example 1: Modify an integration account</span></span>
```
PS C:\>Set-AzIntegrationAccount -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -Sku "Free"
Id          : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31
Name        : IntegrationAccount31
Type        : Microsoft.Logic/integrationAccounts
Location    : brazilsouth
Sku         : 
CreatedTime : 3/26/2016 4:26:07 PM
ChangedTime : 3/26/2016 4:26:07 PM
```

<span data-ttu-id="0a049-114">To polecenie modyfikuje konto integracyjne o nazwie IntegrationAccount31 w określonej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="0a049-114">This command modifies an integration account named IntegrationAccount31 in the specified resource group.</span></span>

## <span data-ttu-id="0a049-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0a049-115">PARAMETERS</span></span>

### <span data-ttu-id="0a049-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a049-116">-DefaultProfile</span></span>
<span data-ttu-id="0a049-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="0a049-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0a049-118">-Force</span><span class="sxs-lookup"><span data-stu-id="0a049-118">-Force</span></span>
<span data-ttu-id="0a049-119">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="0a049-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="0a049-120">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="0a049-120">-Location</span></span>
<span data-ttu-id="0a049-121">Określa lokalizację konta integracji.</span><span class="sxs-lookup"><span data-stu-id="0a049-121">Specifies a location for the integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a049-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="0a049-122">-Name</span></span>
<span data-ttu-id="0a049-123">Określa nazwę konta integracji.</span><span class="sxs-lookup"><span data-stu-id="0a049-123">Specifies the name of the integration account.</span></span>

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

### <span data-ttu-id="0a049-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a049-124">-ResourceGroupName</span></span>
<span data-ttu-id="0a049-125">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="0a049-125">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="0a049-126">-SKU</span><span class="sxs-lookup"><span data-stu-id="0a049-126">-Sku</span></span>
<span data-ttu-id="0a049-127">Określa nazwę jednostki SKU dla konta integracji.</span><span class="sxs-lookup"><span data-stu-id="0a049-127">Specifies a SKU name for the integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Free, Basic, Standard

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a049-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0a049-128">-Confirm</span></span>
<span data-ttu-id="0a049-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0a049-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0a049-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0a049-130">-WhatIf</span></span>
<span data-ttu-id="0a049-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0a049-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0a049-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="0a049-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0a049-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a049-133">CommonParameters</span></span>
<span data-ttu-id="0a049-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0a049-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a049-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0a049-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a049-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0a049-136">INPUTS</span></span>

### <span data-ttu-id="0a049-137">System. String</span><span class="sxs-lookup"><span data-stu-id="0a049-137">System.String</span></span>

## <span data-ttu-id="0a049-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0a049-138">OUTPUTS</span></span>

### <span data-ttu-id="0a049-139">Microsoft. Azure. Management. Logic. MODELES. IntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="0a049-139">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span></span>

## <span data-ttu-id="0a049-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0a049-140">NOTES</span></span>

## <span data-ttu-id="0a049-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0a049-141">RELATED LINKS</span></span>

[<span data-ttu-id="0a049-142">Get-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="0a049-142">Get-AzIntegrationAccount</span></span>](./Get-AzIntegrationAccount.md)

[<span data-ttu-id="0a049-143">Nowe — AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="0a049-143">New-AzIntegrationAccount</span></span>](./New-AzIntegrationAccount.md)

[<span data-ttu-id="0a049-144">Remove-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="0a049-144">Remove-AzIntegrationAccount</span></span>](./Remove-AzIntegrationAccount.md)


