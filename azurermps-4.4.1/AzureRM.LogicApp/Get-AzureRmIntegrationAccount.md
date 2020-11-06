---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 7BCF2086-05FA-43FB-9D19-7277374CB03E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmIntegrationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmIntegrationAccount.md
ms.openlocfilehash: 441681cd33fe7715fbbb6fb244848c287f14ebb6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527522"
---
# <span data-ttu-id="7a7e3-101">Get-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="7a7e3-101">Get-AzureRmIntegrationAccount</span></span>

## <span data-ttu-id="7a7e3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7a7e3-102">SYNOPSIS</span></span>
<span data-ttu-id="7a7e3-103">Pobiera konta integracji.</span><span class="sxs-lookup"><span data-stu-id="7a7e3-103">Gets integration accounts.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7a7e3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7a7e3-104">SYNTAX</span></span>

```
Get-AzureRmIntegrationAccount [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7a7e3-105">Opis</span><span class="sxs-lookup"><span data-stu-id="7a7e3-105">DESCRIPTION</span></span>
<span data-ttu-id="7a7e3-106">Polecenie cmdlet **Get-AzureRmIntegrationAccount** pobiera konta integracji z grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="7a7e3-106">The **Get-AzureRmIntegrationAccount** cmdlet gets integration accounts from a resource group.</span></span> <span data-ttu-id="7a7e3-107">Określ nazwę konta integracji i nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="7a7e3-107">Specify an integration account name and resource group name.</span></span>

<span data-ttu-id="7a7e3-108">Ten moduł obsługuje parametry dynamiczne.</span><span class="sxs-lookup"><span data-stu-id="7a7e3-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="7a7e3-109">Aby użyć parametru dynamicznego, wpisz go w poleceniu.</span><span class="sxs-lookup"><span data-stu-id="7a7e3-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="7a7e3-110">Aby wykryć nazwy parametrów dynamicznych, wpisz znak łącznika (-) po nazwie polecenia cmdlet, a następnie naciskaj klawisz Tab, aby przechodzić między dostępnymi parametrami.</span><span class="sxs-lookup"><span data-stu-id="7a7e3-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="7a7e3-111">W przypadku pominięcia wymaganego parametru szablonu polecenie cmdlet monituje o podanie wartości.</span><span class="sxs-lookup"><span data-stu-id="7a7e3-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="7a7e3-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7a7e3-112">EXAMPLES</span></span>

### <span data-ttu-id="7a7e3-113">Przykład 1: Uzyskaj konto integracyjne według nazwy</span><span class="sxs-lookup"><span data-stu-id="7a7e3-113">Example 1: Get an integration account by name</span></span>
```
PS C:\>Get-AzureRmIntegrationAccount -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31"
Id          : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31
Name        : IntegrationAccount31
Type        : Microsoft.Logic/integrationAccounts
Location    : brazilsouth
Sku         : 
CreatedTime : 3/26/2016 4:26:07 PM
ChangedTime : 3/26/2016 4:26:07 PM
```

<span data-ttu-id="7a7e3-114">To polecenie otrzymuje konto integracyjne o nazwie IntegrationAccount31 z określonej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="7a7e3-114">This command gets an integration account named IntegrationAccount31 from the specified resource group.</span></span>

### <span data-ttu-id="7a7e3-115">Przykład 2: uzyskiwanie kont integracyjnych w grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="7a7e3-115">Example 2: Get integration accounts in a resource group</span></span>
```
PS C:\>Get-AzureRmIntegrationAccount -ResourceGroupName "ResourceGroup11"
Id          : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup1/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31
Name        : IntegrationAccount31
Type        : Microsoft.Logic/integrationAccounts
Location    : brazilsouth
Sku         : 
CreatedTime : 3/26/2016 4:26:07 PM
ChangedTime : 3/26/2016 4:26:07 PM
```

<span data-ttu-id="7a7e3-116">To polecenie pobiera konta integracji z grupy zasobów o nazwie ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="7a7e3-116">This command gets integration accounts from a resource group named ResourceGroup11.</span></span>

### <span data-ttu-id="7a7e3-117">Przykład 3: uzyskiwanie wszystkich kont integracji</span><span class="sxs-lookup"><span data-stu-id="7a7e3-117">Example 3: Get all integration accounts</span></span>
```
PS C:\>Get-AzureRmIntegrationAccount
Id          : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31
Name        : IntegrationAccount31
Type        : Microsoft.Logic/integrationAccounts
Location    : brazilsouth
Sku         : 
CreatedTime : 3/26/2016 4:26:07 PM
ChangedTime : 3/26/2016 4:26:07 PM
```

<span data-ttu-id="7a7e3-118">To polecenie pobiera wszystkie konta integracji w ramach Twojej subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="7a7e3-118">This command gets all the integration accounts in your Azure subscription.</span></span>

## <span data-ttu-id="7a7e3-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7a7e3-119">PARAMETERS</span></span>

### <span data-ttu-id="7a7e3-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="7a7e3-120">-Name</span></span>
<span data-ttu-id="7a7e3-121">Określa nazwę konta integracji.</span><span class="sxs-lookup"><span data-stu-id="7a7e3-121">Specifies the name of an integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a7e3-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a7e3-122">-ResourceGroupName</span></span>
<span data-ttu-id="7a7e3-123">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="7a7e3-123">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="7a7e3-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a7e3-124">-DefaultProfile</span></span>
<span data-ttu-id="7a7e3-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7a7e3-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7a7e3-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a7e3-126">CommonParameters</span></span>
<span data-ttu-id="7a7e3-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a7e3-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a7e3-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7a7e3-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a7e3-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7a7e3-129">INPUTS</span></span>

## <span data-ttu-id="7a7e3-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7a7e3-130">OUTPUTS</span></span>

### <span data-ttu-id="7a7e3-131">Microsoft. Azure. Management. Logic. MODELES. IntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="7a7e3-131">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span></span>

## <span data-ttu-id="7a7e3-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7a7e3-132">NOTES</span></span>

## <span data-ttu-id="7a7e3-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7a7e3-133">RELATED LINKS</span></span>

[<span data-ttu-id="7a7e3-134">Get-AzureRmIntegrationAccountCallbackUrl</span><span class="sxs-lookup"><span data-stu-id="7a7e3-134">Get-AzureRmIntegrationAccountCallbackUrl</span></span>](./Get-AzureRmIntegrationAccountCallbackUrl.md)

[<span data-ttu-id="7a7e3-135">Nowe — AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="7a7e3-135">New-AzureRmIntegrationAccount</span></span>](./New-AzureRmIntegrationAccount.md)

[<span data-ttu-id="7a7e3-136">Remove-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="7a7e3-136">Remove-AzureRmIntegrationAccount</span></span>](./Remove-AzureRmIntegrationAccount.md)

[<span data-ttu-id="7a7e3-137">Set-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="7a7e3-137">Set-AzureRmIntegrationAccount</span></span>](./Set-AzureRmIntegrationAccount.md)


