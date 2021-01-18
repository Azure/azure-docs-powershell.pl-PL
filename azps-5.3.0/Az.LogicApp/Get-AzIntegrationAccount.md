---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 7BCF2086-05FA-43FB-9D19-7277374CB03E
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azintegrationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccount.md
ms.openlocfilehash: b13e7b63994f71f51f321428472169aea52e92f5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98503338"
---
# <span data-ttu-id="1353d-101">Get-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="1353d-101">Get-AzIntegrationAccount</span></span>

## <span data-ttu-id="1353d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1353d-102">SYNOPSIS</span></span>
<span data-ttu-id="1353d-103">Pobiera konta integracji.</span><span class="sxs-lookup"><span data-stu-id="1353d-103">Gets integration accounts.</span></span>

## <span data-ttu-id="1353d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1353d-104">SYNTAX</span></span>

```
Get-AzIntegrationAccount [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1353d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="1353d-105">DESCRIPTION</span></span>
<span data-ttu-id="1353d-106">Polecenie cmdlet **Get-AzIntegrationAccount** pobiera konta integracji z grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="1353d-106">The **Get-AzIntegrationAccount** cmdlet gets integration accounts from a resource group.</span></span> <span data-ttu-id="1353d-107">Określ nazwę konta integracji i nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="1353d-107">Specify an integration account name and resource group name.</span></span>
<span data-ttu-id="1353d-108">Ten moduł obsługuje parametry dynamiczne.</span><span class="sxs-lookup"><span data-stu-id="1353d-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="1353d-109">Aby użyć parametru dynamicznego, wpisz go w poleceniu.</span><span class="sxs-lookup"><span data-stu-id="1353d-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="1353d-110">Aby wykryć nazwy parametrów dynamicznych, wpisz znak łącznika (-) po nazwie polecenia cmdlet, a następnie naciskaj klawisz Tab, aby przechodzić między dostępnymi parametrami.</span><span class="sxs-lookup"><span data-stu-id="1353d-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="1353d-111">W przypadku pominięcia wymaganego parametru szablonu polecenie cmdlet monituje o podanie wartości.</span><span class="sxs-lookup"><span data-stu-id="1353d-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="1353d-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1353d-112">EXAMPLES</span></span>

### <span data-ttu-id="1353d-113">Przykład 1: Uzyskaj konto integracyjne według nazwy</span><span class="sxs-lookup"><span data-stu-id="1353d-113">Example 1: Get an integration account by name</span></span>
```
PS C:\>Get-AzIntegrationAccount -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31"
Id          : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31
Name        : IntegrationAccount31
Type        : Microsoft.Logic/integrationAccounts
Location    : brazilsouth
Sku         : 
CreatedTime : 3/26/2016 4:26:07 PM
ChangedTime : 3/26/2016 4:26:07 PM
```

<span data-ttu-id="1353d-114">To polecenie otrzymuje konto integracyjne o nazwie IntegrationAccount31 z określonej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="1353d-114">This command gets an integration account named IntegrationAccount31 from the specified resource group.</span></span>

### <span data-ttu-id="1353d-115">Przykład 2: uzyskiwanie kont integracyjnych w grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="1353d-115">Example 2: Get integration accounts in a resource group</span></span>
```
PS C:\>Get-AzIntegrationAccount -ResourceGroupName "ResourceGroup11"
Id          : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup1/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31
Name        : IntegrationAccount31
Type        : Microsoft.Logic/integrationAccounts
Location    : brazilsouth
Sku         : 
CreatedTime : 3/26/2016 4:26:07 PM
ChangedTime : 3/26/2016 4:26:07 PM
```

<span data-ttu-id="1353d-116">To polecenie pobiera konta integracji z grupy zasobów o nazwie ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="1353d-116">This command gets integration accounts from a resource group named ResourceGroup11.</span></span>

### <span data-ttu-id="1353d-117">Przykład 3: uzyskiwanie wszystkich kont integracji</span><span class="sxs-lookup"><span data-stu-id="1353d-117">Example 3: Get all integration accounts</span></span>
```
PS C:\>Get-AzIntegrationAccount
Id          : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31
Name        : IntegrationAccount31
Type        : Microsoft.Logic/integrationAccounts
Location    : brazilsouth
Sku         : 
CreatedTime : 3/26/2016 4:26:07 PM
ChangedTime : 3/26/2016 4:26:07 PM
```

<span data-ttu-id="1353d-118">To polecenie pobiera wszystkie konta integracji w ramach Twojej subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="1353d-118">This command gets all the integration accounts in your Azure subscription.</span></span>

## <span data-ttu-id="1353d-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1353d-119">PARAMETERS</span></span>

### <span data-ttu-id="1353d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1353d-120">-DefaultProfile</span></span>
<span data-ttu-id="1353d-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="1353d-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1353d-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="1353d-122">-Name</span></span>
<span data-ttu-id="1353d-123">Określa nazwę konta integracji.</span><span class="sxs-lookup"><span data-stu-id="1353d-123">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="1353d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1353d-124">-ResourceGroupName</span></span>
<span data-ttu-id="1353d-125">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="1353d-125">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="1353d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1353d-126">CommonParameters</span></span>
<span data-ttu-id="1353d-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1353d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1353d-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1353d-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1353d-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1353d-129">INPUTS</span></span>

### <span data-ttu-id="1353d-130">System. String</span><span class="sxs-lookup"><span data-stu-id="1353d-130">System.String</span></span>

## <span data-ttu-id="1353d-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1353d-131">OUTPUTS</span></span>

### <span data-ttu-id="1353d-132">Microsoft. Azure. Management. Logic. MODELES. IntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="1353d-132">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span></span>

## <span data-ttu-id="1353d-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1353d-133">NOTES</span></span>

## <span data-ttu-id="1353d-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1353d-134">RELATED LINKS</span></span>

[<span data-ttu-id="1353d-135">Get-AzIntegrationAccountCallbackUrl</span><span class="sxs-lookup"><span data-stu-id="1353d-135">Get-AzIntegrationAccountCallbackUrl</span></span>](./Get-AzIntegrationAccountCallbackUrl.md)

[<span data-ttu-id="1353d-136">Nowe — AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="1353d-136">New-AzIntegrationAccount</span></span>](./New-AzIntegrationAccount.md)

[<span data-ttu-id="1353d-137">Remove-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="1353d-137">Remove-AzIntegrationAccount</span></span>](./Remove-AzIntegrationAccount.md)

[<span data-ttu-id="1353d-138">Set-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="1353d-138">Set-AzIntegrationAccount</span></span>](./Set-AzIntegrationAccount.md)


