---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 4F65A8B3-A250-41C1-9AA5-DBEB3193C401
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azintegrationaccountmap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountMap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountMap.md
ms.openlocfilehash: 99f6bcda0360395826dedc02e3d8b968ee23795d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94234639"
---
# <span data-ttu-id="25a24-101">Get-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="25a24-101">Get-AzIntegrationAccountMap</span></span>

## <span data-ttu-id="25a24-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="25a24-102">SYNOPSIS</span></span>
<span data-ttu-id="25a24-103">Umożliwia wyświetlenie mapy konta integracji.</span><span class="sxs-lookup"><span data-stu-id="25a24-103">Gets an integration account map.</span></span>

## <span data-ttu-id="25a24-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="25a24-104">SYNTAX</span></span>

```
Get-AzIntegrationAccountMap [-ResourceGroupName <String>] [-Name <String>] [-MapName <String>]
 [-MapType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="25a24-105">Opis</span><span class="sxs-lookup"><span data-stu-id="25a24-105">DESCRIPTION</span></span>
<span data-ttu-id="25a24-106">Polecenie cmdlet **Get-AzIntegrationAccountMap** pobiera mapę konta integracji z grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="25a24-106">The **Get-AzIntegrationAccountMap** cmdlet gets integration account map from a resource group.</span></span>
<span data-ttu-id="25a24-107">Określanie nazwy konta integracji, nazwy grupy zasobów i nazwy mapy.</span><span class="sxs-lookup"><span data-stu-id="25a24-107">Specifying the integration account name, resource group name, and map name.</span></span>
<span data-ttu-id="25a24-108">Ten moduł obsługuje parametry dynamiczne.</span><span class="sxs-lookup"><span data-stu-id="25a24-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="25a24-109">Aby użyć parametru dynamicznego, wpisz go w poleceniu.</span><span class="sxs-lookup"><span data-stu-id="25a24-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="25a24-110">Aby wykryć nazwy parametrów dynamicznych, wpisz znak łącznika (-) po nazwie polecenia cmdlet, a następnie naciskaj klawisz Tab, aby przechodzić między dostępnymi parametrami.</span><span class="sxs-lookup"><span data-stu-id="25a24-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="25a24-111">W przypadku pominięcia wymaganego parametru szablonu polecenie cmdlet monituje o podanie wartości.</span><span class="sxs-lookup"><span data-stu-id="25a24-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="25a24-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="25a24-112">EXAMPLES</span></span>

### <span data-ttu-id="25a24-113">Przykład 1: Pobieranie mapy konta integracji</span><span class="sxs-lookup"><span data-stu-id="25a24-113">Example 1: Get an integration account map</span></span>
```
PS C:\>Get-AzIntegrationAccountMap -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -MapName "IntegrationAccountMap47"
Id                   : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/maps/IntegrationAccountMap47
Name                 : IntegrationAccountMap47
Type                 : Microsoft.Logic/integrationAccounts/maps
CreatedTime          : 3/24/2016 10:34:26 PM
ChangedTime          : 3/24/2016 10:34:26 PM
MapType              : Xslt
ContentType          : 
ContentLink          : https://<baseurl>/integrationaccounts8811f0155a364b5e9618ba28f7180601/99D1E_XSLT_INTEGRATIONACCOUNT
                       MAP1-9A960F9B71C844CDB09D4922B3BCFF61?sv=2014-02-14&sr=b&sig=<value>
ContentSize          : 3056
Metadata             :
```

<span data-ttu-id="25a24-114">To polecenie umożliwia wyświetlenie mapy konta integracji o nazwie IntegrationAccountMap47 w określonej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="25a24-114">This command gets an integration account map named IntegrationAccountMap47 in the specified resource group.</span></span>

### <span data-ttu-id="25a24-115">Przykład 2: Uzyskaj mapowanie konta integracji według nazwy konta integracji</span><span class="sxs-lookup"><span data-stu-id="25a24-115">Example 2: Get integration account maps by integration account name</span></span>
```
PS C:\>Get-AzIntegrationAccountMap -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31"
Id                   : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/maps/IntegrationAccountMap47
Name                 : IntegrationAccountMap47
Type                 : Microsoft.Logic/integrationAccounts/maps
CreatedTime          : 3/24/2016 10:34:26 PM
ChangedTime          : 3/24/2016 10:34:26 PM
MapType              : Xslt
ContentType          : 
ContentLink          : https://<baseurl>/integrationaccounts8811f0155a364b5e9618ba28f7180601/99D1E_XSLT_INTEGRATIONACCOUNT
                       MAP1-9A960F9B71C844CDB09D4922B3BCFF61?sv=2014-02-14&sr=b&sig=<value>
ContentSize          : 3056
Metadata             :
```

<span data-ttu-id="25a24-116">To polecenie pobiera nazwę mapowania kont integracji według nazwy konta.</span><span class="sxs-lookup"><span data-stu-id="25a24-116">This command gets the integration account maps by integration account name.</span></span>

## <span data-ttu-id="25a24-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="25a24-117">PARAMETERS</span></span>

### <span data-ttu-id="25a24-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25a24-118">-DefaultProfile</span></span>
<span data-ttu-id="25a24-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="25a24-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="25a24-120">-MapName</span><span class="sxs-lookup"><span data-stu-id="25a24-120">-MapName</span></span>
<span data-ttu-id="25a24-121">Określa nazwę mapy konta integracji.</span><span class="sxs-lookup"><span data-stu-id="25a24-121">Specifies the name of an integration account map.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25a24-122">-MapType</span><span class="sxs-lookup"><span data-stu-id="25a24-122">-MapType</span></span>
<span data-ttu-id="25a24-123">Typ mapy konta integracji.</span><span class="sxs-lookup"><span data-stu-id="25a24-123">The integration account map type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Xslt, Xslt20, Xslt30, Liquid

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25a24-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="25a24-124">-Name</span></span>
<span data-ttu-id="25a24-125">Określa nazwę konta integracji.</span><span class="sxs-lookup"><span data-stu-id="25a24-125">Specifies the name for the integration account.</span></span>

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

### <span data-ttu-id="25a24-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25a24-126">-ResourceGroupName</span></span>
<span data-ttu-id="25a24-127">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="25a24-127">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="25a24-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25a24-128">CommonParameters</span></span>
<span data-ttu-id="25a24-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25a24-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25a24-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="25a24-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25a24-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="25a24-131">INPUTS</span></span>

### <span data-ttu-id="25a24-132">System. String</span><span class="sxs-lookup"><span data-stu-id="25a24-132">System.String</span></span>

## <span data-ttu-id="25a24-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="25a24-133">OUTPUTS</span></span>

### <span data-ttu-id="25a24-134">Microsoft. Azure. Management. Logic. MODELES. IntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="25a24-134">Microsoft.Azure.Management.Logic.Models.IntegrationAccountMap</span></span>

## <span data-ttu-id="25a24-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="25a24-135">NOTES</span></span>

## <span data-ttu-id="25a24-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="25a24-136">RELATED LINKS</span></span>

[<span data-ttu-id="25a24-137">Nowe — AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="25a24-137">New-AzIntegrationAccountMap</span></span>](./New-AzIntegrationAccountMap.md)

[<span data-ttu-id="25a24-138">Remove-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="25a24-138">Remove-AzIntegrationAccountMap</span></span>](./Remove-AzIntegrationAccountMap.md)

[<span data-ttu-id="25a24-139">Set-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="25a24-139">Set-AzIntegrationAccountMap</span></span>](./Set-AzIntegrationAccountMap.md)


