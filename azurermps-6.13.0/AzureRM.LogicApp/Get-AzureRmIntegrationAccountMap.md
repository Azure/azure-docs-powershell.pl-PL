---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 4F65A8B3-A250-41C1-9AA5-DBEB3193C401
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/get-azurermintegrationaccountmap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmIntegrationAccountMap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmIntegrationAccountMap.md
ms.openlocfilehash: f56878ac2aa2f625b5583805150fd16368d9f718
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93552779"
---
# <span data-ttu-id="aa4f0-101">Get-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="aa4f0-101">Get-AzureRmIntegrationAccountMap</span></span>

## <span data-ttu-id="aa4f0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="aa4f0-102">SYNOPSIS</span></span>
<span data-ttu-id="aa4f0-103">Umożliwia wyświetlenie mapy konta integracji.</span><span class="sxs-lookup"><span data-stu-id="aa4f0-103">Gets an integration account map.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aa4f0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="aa4f0-104">SYNTAX</span></span>

```
Get-AzureRmIntegrationAccountMap [-ResourceGroupName <String>] [-Name <String>] [-MapName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aa4f0-105">Opis</span><span class="sxs-lookup"><span data-stu-id="aa4f0-105">DESCRIPTION</span></span>
<span data-ttu-id="aa4f0-106">Polecenie cmdlet **Get-AzureRmIntegrationAccountMap** pobiera mapę konta integracji z grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="aa4f0-106">The **Get-AzureRmIntegrationAccountMap** cmdlet gets integration account map from a resource group.</span></span>
<span data-ttu-id="aa4f0-107">Określanie nazwy konta integracji, nazwy grupy zasobów i nazwy mapy.</span><span class="sxs-lookup"><span data-stu-id="aa4f0-107">Specifying the integration account name, resource group name, and map name.</span></span>
<span data-ttu-id="aa4f0-108">Ten moduł obsługuje parametry dynamiczne.</span><span class="sxs-lookup"><span data-stu-id="aa4f0-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="aa4f0-109">Aby użyć parametru dynamicznego, wpisz go w poleceniu.</span><span class="sxs-lookup"><span data-stu-id="aa4f0-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="aa4f0-110">Aby wykryć nazwy parametrów dynamicznych, wpisz znak łącznika (-) po nazwie polecenia cmdlet, a następnie naciskaj klawisz Tab, aby przechodzić między dostępnymi parametrami.</span><span class="sxs-lookup"><span data-stu-id="aa4f0-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="aa4f0-111">W przypadku pominięcia wymaganego parametru szablonu polecenie cmdlet monituje o podanie wartości.</span><span class="sxs-lookup"><span data-stu-id="aa4f0-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="aa4f0-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="aa4f0-112">EXAMPLES</span></span>

### <span data-ttu-id="aa4f0-113">Przykład 1: Pobieranie mapy konta integracji</span><span class="sxs-lookup"><span data-stu-id="aa4f0-113">Example 1: Get an integration account map</span></span>
```
PS C:\>Get-AzureRmIntegrationAccountMap -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -MapName "IntegrationAccountMap47"
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

<span data-ttu-id="aa4f0-114">To polecenie umożliwia wyświetlenie mapy konta integracji o nazwie IntegrationAccountMap47 w określonej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="aa4f0-114">This command gets an integration account map named IntegrationAccountMap47 in the specified resource group.</span></span>

### <span data-ttu-id="aa4f0-115">Przykład 2: Uzyskaj mapowanie konta integracji według nazwy konta integracji</span><span class="sxs-lookup"><span data-stu-id="aa4f0-115">Example 2: Get integration account maps by integration account name</span></span>
```
PS C:\>Get-AzureRmIntegrationAccountMap -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31"
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

<span data-ttu-id="aa4f0-116">To polecenie pobiera nazwę mapowania kont integracji według nazwy konta.</span><span class="sxs-lookup"><span data-stu-id="aa4f0-116">This command gets the integration account maps by integration account name.</span></span>

## <span data-ttu-id="aa4f0-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="aa4f0-117">PARAMETERS</span></span>

### <span data-ttu-id="aa4f0-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa4f0-118">-DefaultProfile</span></span>
<span data-ttu-id="aa4f0-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="aa4f0-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="aa4f0-120">-MapName</span><span class="sxs-lookup"><span data-stu-id="aa4f0-120">-MapName</span></span>
<span data-ttu-id="aa4f0-121">Określa nazwę mapy konta integracji.</span><span class="sxs-lookup"><span data-stu-id="aa4f0-121">Specifies the name of an integration account map.</span></span>

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

### <span data-ttu-id="aa4f0-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="aa4f0-122">-Name</span></span>
<span data-ttu-id="aa4f0-123">Określa nazwę konta integracji.</span><span class="sxs-lookup"><span data-stu-id="aa4f0-123">Specifies the name for the integration account.</span></span>

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

### <span data-ttu-id="aa4f0-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa4f0-124">-ResourceGroupName</span></span>
<span data-ttu-id="aa4f0-125">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="aa4f0-125">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="aa4f0-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa4f0-126">CommonParameters</span></span>
<span data-ttu-id="aa4f0-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aa4f0-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa4f0-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aa4f0-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa4f0-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="aa4f0-129">INPUTS</span></span>

### <span data-ttu-id="aa4f0-130">System. String</span><span class="sxs-lookup"><span data-stu-id="aa4f0-130">System.String</span></span>

## <span data-ttu-id="aa4f0-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="aa4f0-131">OUTPUTS</span></span>

### <span data-ttu-id="aa4f0-132">Microsoft. Azure. Management. Logic. MODELES. IntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="aa4f0-132">Microsoft.Azure.Management.Logic.Models.IntegrationAccountMap</span></span>

## <span data-ttu-id="aa4f0-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="aa4f0-133">NOTES</span></span>

## <span data-ttu-id="aa4f0-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="aa4f0-134">RELATED LINKS</span></span>

[<span data-ttu-id="aa4f0-135">Nowe — AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="aa4f0-135">New-AzureRmIntegrationAccountMap</span></span>](./New-AzureRmIntegrationAccountMap.md)

[<span data-ttu-id="aa4f0-136">Remove-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="aa4f0-136">Remove-AzureRmIntegrationAccountMap</span></span>](./Remove-AzureRmIntegrationAccountMap.md)

[<span data-ttu-id="aa4f0-137">Set-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="aa4f0-137">Set-AzureRmIntegrationAccountMap</span></span>](./Set-AzureRmIntegrationAccountMap.md)


