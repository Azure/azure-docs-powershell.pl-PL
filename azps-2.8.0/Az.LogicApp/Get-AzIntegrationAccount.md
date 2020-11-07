---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 7BCF2086-05FA-43FB-9D19-7277374CB03E
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azintegrationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccount.md
ms.openlocfilehash: bf57ffe0823ced37eaf58e9321c4330002c9be48
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93705061"
---
# <span data-ttu-id="addac-101">Get-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="addac-101">Get-AzIntegrationAccount</span></span>

## <span data-ttu-id="addac-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="addac-102">SYNOPSIS</span></span>
<span data-ttu-id="addac-103">Pobiera konta integracji.</span><span class="sxs-lookup"><span data-stu-id="addac-103">Gets integration accounts.</span></span>

## <span data-ttu-id="addac-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="addac-104">SYNTAX</span></span>

```
Get-AzIntegrationAccount [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="addac-105">Opis</span><span class="sxs-lookup"><span data-stu-id="addac-105">DESCRIPTION</span></span>
<span data-ttu-id="addac-106">Polecenie cmdlet **Get-AzIntegrationAccount** pobiera konta integracji z grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="addac-106">The **Get-AzIntegrationAccount** cmdlet gets integration accounts from a resource group.</span></span> <span data-ttu-id="addac-107">Określ nazwę konta integracji i nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="addac-107">Specify an integration account name and resource group name.</span></span>
<span data-ttu-id="addac-108">Ten moduł obsługuje parametry dynamiczne.</span><span class="sxs-lookup"><span data-stu-id="addac-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="addac-109">Aby użyć parametru dynamicznego, wpisz go w poleceniu.</span><span class="sxs-lookup"><span data-stu-id="addac-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="addac-110">Aby wykryć nazwy parametrów dynamicznych, wpisz znak łącznika (-) po nazwie polecenia cmdlet, a następnie naciskaj klawisz Tab, aby przechodzić między dostępnymi parametrami.</span><span class="sxs-lookup"><span data-stu-id="addac-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="addac-111">W przypadku pominięcia wymaganego parametru szablonu polecenie cmdlet monituje o podanie wartości.</span><span class="sxs-lookup"><span data-stu-id="addac-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="addac-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="addac-112">EXAMPLES</span></span>

### <span data-ttu-id="addac-113">Przykład 1: Uzyskaj konto integracyjne według nazwy</span><span class="sxs-lookup"><span data-stu-id="addac-113">Example 1: Get an integration account by name</span></span>
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

<span data-ttu-id="addac-114">To polecenie otrzymuje konto integracyjne o nazwie IntegrationAccount31 z określonej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="addac-114">This command gets an integration account named IntegrationAccount31 from the specified resource group.</span></span>

### <span data-ttu-id="addac-115">Przykład 2: uzyskiwanie kont integracyjnych w grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="addac-115">Example 2: Get integration accounts in a resource group</span></span>
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

<span data-ttu-id="addac-116">To polecenie pobiera konta integracji z grupy zasobów o nazwie ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="addac-116">This command gets integration accounts from a resource group named ResourceGroup11.</span></span>

### <span data-ttu-id="addac-117">Przykład 3: uzyskiwanie wszystkich kont integracji</span><span class="sxs-lookup"><span data-stu-id="addac-117">Example 3: Get all integration accounts</span></span>
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

<span data-ttu-id="addac-118">To polecenie pobiera wszystkie konta integracji w ramach Twojej subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="addac-118">This command gets all the integration accounts in your Azure subscription.</span></span>

## <span data-ttu-id="addac-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="addac-119">PARAMETERS</span></span>

### <span data-ttu-id="addac-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="addac-120">-DefaultProfile</span></span>
<span data-ttu-id="addac-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="addac-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="addac-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="addac-122">-Name</span></span>
<span data-ttu-id="addac-123">Określa nazwę konta integracji.</span><span class="sxs-lookup"><span data-stu-id="addac-123">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="addac-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="addac-124">-ResourceGroupName</span></span>
<span data-ttu-id="addac-125">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="addac-125">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="addac-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="addac-126">CommonParameters</span></span>
<span data-ttu-id="addac-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="addac-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="addac-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="addac-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="addac-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="addac-129">INPUTS</span></span>

### <span data-ttu-id="addac-130">System. String</span><span class="sxs-lookup"><span data-stu-id="addac-130">System.String</span></span>

## <span data-ttu-id="addac-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="addac-131">OUTPUTS</span></span>

### <span data-ttu-id="addac-132">Microsoft. Azure. Management. Logic. MODELES. IntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="addac-132">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span></span>

## <span data-ttu-id="addac-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="addac-133">NOTES</span></span>

## <span data-ttu-id="addac-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="addac-134">RELATED LINKS</span></span>

[<span data-ttu-id="addac-135">Get-AzIntegrationAccountCallbackUrl</span><span class="sxs-lookup"><span data-stu-id="addac-135">Get-AzIntegrationAccountCallbackUrl</span></span>](./Get-AzIntegrationAccountCallbackUrl.md)

[<span data-ttu-id="addac-136">Nowe — AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="addac-136">New-AzIntegrationAccount</span></span>](./New-AzIntegrationAccount.md)

[<span data-ttu-id="addac-137">Remove-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="addac-137">Remove-AzIntegrationAccount</span></span>](./Remove-AzIntegrationAccount.md)

[<span data-ttu-id="addac-138">Set-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="addac-138">Set-AzIntegrationAccount</span></span>](./Set-AzIntegrationAccount.md)


