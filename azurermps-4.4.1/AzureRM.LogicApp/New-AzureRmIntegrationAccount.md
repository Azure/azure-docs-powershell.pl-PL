---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 5F1A4FE0-CB57-45D3-9F08-879469A61E1E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/New-AzureRmIntegrationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/New-AzureRmIntegrationAccount.md
ms.openlocfilehash: ec1e223359c3d83a3cfb77810e0e680f7142bc60
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93550960"
---
# <span data-ttu-id="2b682-101">New-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="2b682-101">New-AzureRmIntegrationAccount</span></span>

## <span data-ttu-id="2b682-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2b682-102">SYNOPSIS</span></span>
<span data-ttu-id="2b682-103">Tworzy konto integracji.</span><span class="sxs-lookup"><span data-stu-id="2b682-103">Creates an integration account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2b682-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2b682-104">SYNTAX</span></span>

```
New-AzureRmIntegrationAccount -ResourceGroupName <String> -Name <String> -Location <String> [-Sku <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2b682-105">Opis</span><span class="sxs-lookup"><span data-stu-id="2b682-105">DESCRIPTION</span></span>
<span data-ttu-id="2b682-106">Polecenie cmdlet **New-AzureRmIntegrationAccount** umożliwia utworzenie konta integracji.</span><span class="sxs-lookup"><span data-stu-id="2b682-106">The **New-AzureRmIntegrationAccount** cmdlet creates an integration account.</span></span>
<span data-ttu-id="2b682-107">To polecenie cmdlet zwraca obiekt reprezentujący konto integracji. Określ nazwę, lokalizację, nazwę grupy zasobów i nazwę jednostki SKU.</span><span class="sxs-lookup"><span data-stu-id="2b682-107">This cmdlet returns an object that represents the integration account.Specify a name, location, resource group name, and SKU name.</span></span>

<span data-ttu-id="2b682-108">Wartości plików parametrów szablonu określone w wierszu polecenia mają pierwszeństwo przed wartościami parametrów szablonu w obiekcie parametru szablonu.</span><span class="sxs-lookup"><span data-stu-id="2b682-108">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>

<span data-ttu-id="2b682-109">Ten moduł obsługuje parametry dynamiczne.</span><span class="sxs-lookup"><span data-stu-id="2b682-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="2b682-110">Aby użyć parametru dynamicznego, wpisz go w poleceniu.</span><span class="sxs-lookup"><span data-stu-id="2b682-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="2b682-111">Aby wykryć nazwy parametrów dynamicznych, wpisz znak łącznika (-) po nazwie polecenia cmdlet, a następnie naciskaj klawisz Tab, aby przechodzić między dostępnymi parametrami.</span><span class="sxs-lookup"><span data-stu-id="2b682-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="2b682-112">W przypadku pominięcia wymaganego parametru szablonu polecenie cmdlet monituje o podanie wartości.</span><span class="sxs-lookup"><span data-stu-id="2b682-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="2b682-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2b682-113">EXAMPLES</span></span>

### <span data-ttu-id="2b682-114">Przykład 1: Tworzenie konta integracyjnego</span><span class="sxs-lookup"><span data-stu-id="2b682-114">Example 1: Create an integration account</span></span>
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

<span data-ttu-id="2b682-115">To polecenie tworzy konto integracyjne o nazwie IntegrationAccount31 w określonej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="2b682-115">This command creates an integration account named IntegrationAccount31 in the specified resource group.</span></span>

## <span data-ttu-id="2b682-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2b682-116">PARAMETERS</span></span>

### <span data-ttu-id="2b682-117">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="2b682-117">-Location</span></span>
<span data-ttu-id="2b682-118">Określa lokalizację konta integracji.</span><span class="sxs-lookup"><span data-stu-id="2b682-118">Specifies a location for the integration account.</span></span>

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

### <span data-ttu-id="2b682-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="2b682-119">-Name</span></span>
<span data-ttu-id="2b682-120">Określa nazwę konta integracyjnego.</span><span class="sxs-lookup"><span data-stu-id="2b682-120">Specifies a name for the integration account.</span></span>

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

### <span data-ttu-id="2b682-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b682-121">-ResourceGroupName</span></span>
<span data-ttu-id="2b682-122">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="2b682-122">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="2b682-123">-SKU</span><span class="sxs-lookup"><span data-stu-id="2b682-123">-Sku</span></span>
<span data-ttu-id="2b682-124">Określa nazwę jednostki SKU dla konta integracji.</span><span class="sxs-lookup"><span data-stu-id="2b682-124">Specifies a SKU name for the integration account.</span></span>

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

### <span data-ttu-id="2b682-125">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2b682-125">-Confirm</span></span>
<span data-ttu-id="2b682-126">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2b682-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2b682-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2b682-127">-WhatIf</span></span>
<span data-ttu-id="2b682-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2b682-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2b682-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="2b682-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2b682-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b682-130">-DefaultProfile</span></span>
<span data-ttu-id="2b682-131">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2b682-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2b682-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b682-132">CommonParameters</span></span>
<span data-ttu-id="2b682-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2b682-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b682-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2b682-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b682-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2b682-135">INPUTS</span></span>

## <span data-ttu-id="2b682-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2b682-136">OUTPUTS</span></span>

### <span data-ttu-id="2b682-137">Microsoft. Azure. Management. Logic. MODELES. IntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="2b682-137">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span></span>

## <span data-ttu-id="2b682-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2b682-138">NOTES</span></span>

## <span data-ttu-id="2b682-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2b682-139">RELATED LINKS</span></span>

[<span data-ttu-id="2b682-140">Get-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="2b682-140">Get-AzureRmIntegrationAccount</span></span>](./Get-AzureRmIntegrationAccount.md)

[<span data-ttu-id="2b682-141">Remove-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="2b682-141">Remove-AzureRmIntegrationAccount</span></span>](./Remove-AzureRmIntegrationAccount.md)

[<span data-ttu-id="2b682-142">Set-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="2b682-142">Set-AzureRmIntegrationAccount</span></span>](./Set-AzureRmIntegrationAccount.md)


