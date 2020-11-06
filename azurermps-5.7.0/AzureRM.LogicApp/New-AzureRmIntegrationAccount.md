---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 5F1A4FE0-CB57-45D3-9F08-879469A61E1E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/new-azurermintegrationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/New-AzureRmIntegrationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/New-AzureRmIntegrationAccount.md
ms.openlocfilehash: 44dc417521b49d47b9c060b987c82ddd06b7f8dc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528114"
---
# <span data-ttu-id="97dc0-101">New-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="97dc0-101">New-AzureRmIntegrationAccount</span></span>

## <span data-ttu-id="97dc0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="97dc0-102">SYNOPSIS</span></span>
<span data-ttu-id="97dc0-103">Tworzy konto integracji.</span><span class="sxs-lookup"><span data-stu-id="97dc0-103">Creates an integration account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="97dc0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="97dc0-104">SYNTAX</span></span>

```
New-AzureRmIntegrationAccount -ResourceGroupName <String> -Name <String> -Location <String> [-Sku <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="97dc0-105">Opis</span><span class="sxs-lookup"><span data-stu-id="97dc0-105">DESCRIPTION</span></span>
<span data-ttu-id="97dc0-106">Polecenie cmdlet **New-AzureRmIntegrationAccount** umożliwia utworzenie konta integracji.</span><span class="sxs-lookup"><span data-stu-id="97dc0-106">The **New-AzureRmIntegrationAccount** cmdlet creates an integration account.</span></span>
<span data-ttu-id="97dc0-107">To polecenie cmdlet zwraca obiekt reprezentujący konto integracji. Określ nazwę, lokalizację, nazwę grupy zasobów i nazwę jednostki SKU.</span><span class="sxs-lookup"><span data-stu-id="97dc0-107">This cmdlet returns an object that represents the integration account.Specify a name, location, resource group name, and SKU name.</span></span>

<span data-ttu-id="97dc0-108">Wartości plików parametrów szablonu określone w wierszu polecenia mają pierwszeństwo przed wartościami parametrów szablonu w obiekcie parametru szablonu.</span><span class="sxs-lookup"><span data-stu-id="97dc0-108">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>

<span data-ttu-id="97dc0-109">Ten moduł obsługuje parametry dynamiczne.</span><span class="sxs-lookup"><span data-stu-id="97dc0-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="97dc0-110">Aby użyć parametru dynamicznego, wpisz go w poleceniu.</span><span class="sxs-lookup"><span data-stu-id="97dc0-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="97dc0-111">Aby wykryć nazwy parametrów dynamicznych, wpisz znak łącznika (-) po nazwie polecenia cmdlet, a następnie naciskaj klawisz Tab, aby przechodzić między dostępnymi parametrami.</span><span class="sxs-lookup"><span data-stu-id="97dc0-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="97dc0-112">W przypadku pominięcia wymaganego parametru szablonu polecenie cmdlet monituje o podanie wartości.</span><span class="sxs-lookup"><span data-stu-id="97dc0-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="97dc0-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="97dc0-113">EXAMPLES</span></span>

### <span data-ttu-id="97dc0-114">Przykład 1: Tworzenie konta integracyjnego</span><span class="sxs-lookup"><span data-stu-id="97dc0-114">Example 1: Create an integration account</span></span>
```
PS C:\>New-AzureRmIntegrationAccount -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -Location "brazilsouth" -Sku "Standard"
Id          : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31
Name        : IntegrationAccount31
Type        : Microsoft.Logic/integrationAccounts
Location    : brazilsouth
Sku         : 
CreatedTime : 3/26/2016 4:26:07 PM
ChangedTime : 3/26/2016 4:26:07 PM
```

<span data-ttu-id="97dc0-115">To polecenie tworzy konto integracyjne o nazwie IntegrationAccount31 w określonej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="97dc0-115">This command creates an integration account named IntegrationAccount31 in the specified resource group.</span></span>

## <span data-ttu-id="97dc0-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="97dc0-116">PARAMETERS</span></span>

### <span data-ttu-id="97dc0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97dc0-117">-DefaultProfile</span></span>
<span data-ttu-id="97dc0-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="97dc0-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="97dc0-119">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="97dc0-119">-Location</span></span>
<span data-ttu-id="97dc0-120">Określa lokalizację konta integracji.</span><span class="sxs-lookup"><span data-stu-id="97dc0-120">Specifies a location for the integration account.</span></span>

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

### <span data-ttu-id="97dc0-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="97dc0-121">-Name</span></span>
<span data-ttu-id="97dc0-122">Określa nazwę konta integracyjnego.</span><span class="sxs-lookup"><span data-stu-id="97dc0-122">Specifies a name for the integration account.</span></span>

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

### <span data-ttu-id="97dc0-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="97dc0-123">-ResourceGroupName</span></span>
<span data-ttu-id="97dc0-124">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="97dc0-124">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="97dc0-125">-SKU</span><span class="sxs-lookup"><span data-stu-id="97dc0-125">-Sku</span></span>
<span data-ttu-id="97dc0-126">Określa nazwę jednostki SKU dla konta integracji.</span><span class="sxs-lookup"><span data-stu-id="97dc0-126">Specifies a SKU name for the integration account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97dc0-127">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="97dc0-127">-Confirm</span></span>
<span data-ttu-id="97dc0-128">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="97dc0-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="97dc0-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="97dc0-129">-WhatIf</span></span>
<span data-ttu-id="97dc0-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="97dc0-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="97dc0-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="97dc0-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="97dc0-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97dc0-132">CommonParameters</span></span>
<span data-ttu-id="97dc0-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97dc0-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97dc0-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="97dc0-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97dc0-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="97dc0-135">INPUTS</span></span>

### <span data-ttu-id="97dc0-136">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="97dc0-136">None</span></span>
<span data-ttu-id="97dc0-137">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="97dc0-137">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="97dc0-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="97dc0-138">OUTPUTS</span></span>

### <span data-ttu-id="97dc0-139">Microsoft. Azure. Management. Logic. MODELES. IntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="97dc0-139">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span></span>

## <span data-ttu-id="97dc0-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="97dc0-140">NOTES</span></span>

## <span data-ttu-id="97dc0-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="97dc0-141">RELATED LINKS</span></span>

[<span data-ttu-id="97dc0-142">Get-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="97dc0-142">Get-AzureRmIntegrationAccount</span></span>](./Get-AzureRmIntegrationAccount.md)

[<span data-ttu-id="97dc0-143">Remove-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="97dc0-143">Remove-AzureRmIntegrationAccount</span></span>](./Remove-AzureRmIntegrationAccount.md)

[<span data-ttu-id="97dc0-144">Set-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="97dc0-144">Set-AzureRmIntegrationAccount</span></span>](./Set-AzureRmIntegrationAccount.md)


