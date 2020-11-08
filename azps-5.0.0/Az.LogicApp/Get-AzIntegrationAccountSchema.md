---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 6C16B04B-459A-4B2C-B7DF-AC4D16FF7281
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azintegrationaccountschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountSchema.md
ms.openlocfilehash: ed85c1fea8bd338b3dd4f2a9e82ee5aac3f3b52b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94234635"
---
# <span data-ttu-id="935f0-101">Get-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="935f0-101">Get-AzIntegrationAccountSchema</span></span>

## <span data-ttu-id="935f0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="935f0-102">SYNOPSIS</span></span>
<span data-ttu-id="935f0-103">Umożliwia pobieranie schematów kont integracji.</span><span class="sxs-lookup"><span data-stu-id="935f0-103">Gets integration account schemas.</span></span>

## <span data-ttu-id="935f0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="935f0-104">SYNTAX</span></span>

```
Get-AzIntegrationAccountSchema [-ResourceGroupName <String>] [-Name <String>] [-SchemaName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="935f0-105">Opis</span><span class="sxs-lookup"><span data-stu-id="935f0-105">DESCRIPTION</span></span>
<span data-ttu-id="935f0-106">Polecenie cmdlet **Get-AzIntegrationAccountSchema** pobiera schematy kont integracji.</span><span class="sxs-lookup"><span data-stu-id="935f0-106">The **Get-AzIntegrationAccountSchema** cmdlet gets integration account schemas.</span></span>
<span data-ttu-id="935f0-107">Określanie nazwy konta integracji, nazwy grupy zasobów i nazwy schematu.</span><span class="sxs-lookup"><span data-stu-id="935f0-107">Specifying the integration account name, resource group name, and schema name.</span></span>
<span data-ttu-id="935f0-108">Ten moduł obsługuje parametry dynamiczne.</span><span class="sxs-lookup"><span data-stu-id="935f0-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="935f0-109">Aby użyć parametru dynamicznego, wpisz go w poleceniu.</span><span class="sxs-lookup"><span data-stu-id="935f0-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="935f0-110">Aby wykryć nazwy parametrów dynamicznych, wpisz znak łącznika (-) po nazwie polecenia cmdlet, a następnie naciskaj klawisz Tab, aby przechodzić między dostępnymi parametrami.</span><span class="sxs-lookup"><span data-stu-id="935f0-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="935f0-111">W przypadku pominięcia wymaganego parametru szablonu polecenie cmdlet monituje o podanie wartości.</span><span class="sxs-lookup"><span data-stu-id="935f0-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="935f0-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="935f0-112">EXAMPLES</span></span>

### <span data-ttu-id="935f0-113">Przykład 1: uzyskiwanie schematu konta integracji</span><span class="sxs-lookup"><span data-stu-id="935f0-113">Example 1: Get an integration account schema</span></span>
```
PS C:\>Get-AzIntegrationAccountSchema -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -SchemaName "IntegrationAccountSchema43"
Id                   : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/schemas/IntegrationAccountSchema43
Name                 : IntegrationAccountSchema43
Type                 : Microsoft.Logic/integrationAccounts/schemas
CreatedTime          : 3/25/2016 5:42:58 PM
ChangedTime          : 3/25/2016 5:42:58 PM
SchemaType           : Xml
ContentType          : 
ContentLink          : https://<baseurl>/integrationaccounts469af4f3cf4047b7ac3a08c87948ec5f/3839E_XML_INTEGRATIONACCOUNTSCHEMA43-5A86631F61F
                       14513AA1185A52C6B2874?sv=2014-02-14&sr=b&sig=<value>
ContentSize          : 7901
MetaData             :
```

<span data-ttu-id="935f0-114">To polecenie umożliwia wyświetlenie schematu konta integracji o nazwie IntegrationAccountSchema43.</span><span class="sxs-lookup"><span data-stu-id="935f0-114">This command gets the integration account schema named IntegrationAccountSchema43.</span></span>

### <span data-ttu-id="935f0-115">Przykład 2: pobieranie schematów kont integracji dla grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="935f0-115">Example 2: Get integration account schemas for a resource group</span></span>
```
PS C:\>Get-AzIntegrationAccountSchema -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31"
Id                   : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/schemas/IntegrationAccountSchema43
Name                 : IntegrationAccountSchema43
Type                 : Microsoft.Logic/integrationAccounts/schemas
CreatedTime          : 3/25/2016 5:42:58 PM
ChangedTime          : 3/25/2016 5:42:58 PM
SchemaType           : Xml
ContentType          : 
ContentLink          : https://<baseurl>/integrationaccounts469af4f3cf4047b7ac3a08c87948ec5f/3839E_XML_INTEGRATIONACCOUNTSCHEMA43-5A86631F61F
                       14513AA1185A52C6B2874?sv=2014-02-14&sr=b&sig=<value>
ContentSize          : 7901
MetaData             :
```

<span data-ttu-id="935f0-116">To polecenie pobiera schematy kont integracyjnych dla grupy zasobów o nazwie ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="935f0-116">This command gets the integration account schemas for the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="935f0-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="935f0-117">PARAMETERS</span></span>

### <span data-ttu-id="935f0-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="935f0-118">-DefaultProfile</span></span>
<span data-ttu-id="935f0-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="935f0-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="935f0-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="935f0-120">-Name</span></span>
<span data-ttu-id="935f0-121">Określa nazwę konta integracji.</span><span class="sxs-lookup"><span data-stu-id="935f0-121">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="935f0-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="935f0-122">-ResourceGroupName</span></span>
<span data-ttu-id="935f0-123">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="935f0-123">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="935f0-124">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="935f0-124">-SchemaName</span></span>
<span data-ttu-id="935f0-125">Określa nazwę schematu konta integracji.</span><span class="sxs-lookup"><span data-stu-id="935f0-125">Specifies the name of an integration account schema.</span></span>
<span data-ttu-id="935f0-126">Określa nazwę schematu.</span><span class="sxs-lookup"><span data-stu-id="935f0-126">Specifies the name of a schema.</span></span>
<span data-ttu-id="935f0-127">.</span><span class="sxs-lookup"><span data-stu-id="935f0-127">.</span></span>

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

### <span data-ttu-id="935f0-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="935f0-128">CommonParameters</span></span>
<span data-ttu-id="935f0-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="935f0-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="935f0-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="935f0-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="935f0-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="935f0-131">INPUTS</span></span>

### <span data-ttu-id="935f0-132">System. String</span><span class="sxs-lookup"><span data-stu-id="935f0-132">System.String</span></span>

## <span data-ttu-id="935f0-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="935f0-133">OUTPUTS</span></span>

### <span data-ttu-id="935f0-134">Microsoft. Azure. Management. Logic. MODELES. IntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="935f0-134">Microsoft.Azure.Management.Logic.Models.IntegrationAccountSchema</span></span>

## <span data-ttu-id="935f0-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="935f0-135">NOTES</span></span>

## <span data-ttu-id="935f0-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="935f0-136">RELATED LINKS</span></span>

[<span data-ttu-id="935f0-137">Nowe — AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="935f0-137">New-AzIntegrationAccountSchema</span></span>](./New-AzIntegrationAccountSchema.md)

[<span data-ttu-id="935f0-138">Remove-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="935f0-138">Remove-AzIntegrationAccountSchema</span></span>](./Remove-AzIntegrationAccountSchema.md)

[<span data-ttu-id="935f0-139">Set-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="935f0-139">Set-AzIntegrationAccountSchema</span></span>](./Set-AzIntegrationAccountSchema.md)


