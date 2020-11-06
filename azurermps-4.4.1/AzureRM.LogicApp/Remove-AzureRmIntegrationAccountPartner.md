---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: E8A557EA-FE3F-4433-BFDE-B4D73DF8467C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Remove-AzureRmIntegrationAccountPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Remove-AzureRmIntegrationAccountPartner.md
ms.openlocfilehash: f10173dce7b64ccc656e2c852c6eb20230d1a7bf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93550951"
---
# <span data-ttu-id="ad399-101">Remove-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="ad399-101">Remove-AzureRmIntegrationAccountPartner</span></span>

## <span data-ttu-id="ad399-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ad399-102">SYNOPSIS</span></span>
<span data-ttu-id="ad399-103">Usuwa partnera kont integracji.</span><span class="sxs-lookup"><span data-stu-id="ad399-103">Removes an integration account partner.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ad399-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ad399-104">SYNTAX</span></span>

```
Remove-AzureRmIntegrationAccountPartner -ResourceGroupName <String> -Name <String> -PartnerName <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ad399-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ad399-105">DESCRIPTION</span></span>
<span data-ttu-id="ad399-106">Polecenie cmdlet **Remove-AzureRmIntegrationAccountPartner** umożliwia usunięcie partnera konta integracji z grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="ad399-106">The **Remove-AzureRmIntegrationAccountPartner** cmdlet removes an integration account partner from a resource group.</span></span>
<span data-ttu-id="ad399-107">Określ nazwę konta integracji, nazwę grupy zasobów i nazwę partnera.</span><span class="sxs-lookup"><span data-stu-id="ad399-107">Specify the integration account name, resource group name, and partner name.</span></span>

<span data-ttu-id="ad399-108">Ten moduł obsługuje parametry dynamiczne.</span><span class="sxs-lookup"><span data-stu-id="ad399-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="ad399-109">Aby użyć parametru dynamicznego, wpisz go w poleceniu.</span><span class="sxs-lookup"><span data-stu-id="ad399-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="ad399-110">Aby wykryć nazwy parametrów dynamicznych, wpisz znak łącznika (-) po nazwie polecenia cmdlet, a następnie naciskaj klawisz Tab, aby przechodzić między dostępnymi parametrami.</span><span class="sxs-lookup"><span data-stu-id="ad399-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="ad399-111">W przypadku pominięcia wymaganego parametru szablonu polecenie cmdlet monituje o podanie wartości.</span><span class="sxs-lookup"><span data-stu-id="ad399-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="ad399-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ad399-112">EXAMPLES</span></span>

### <span data-ttu-id="ad399-113">Przykład 1: usuwanie partnera kont integracji</span><span class="sxs-lookup"><span data-stu-id="ad399-113">Example 1: Remove an integration account partner</span></span>
```
PS C:\>Remove-AzureRmIntegrationAccountPartner -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -PartnerName "IntegrationAccountPartner1"
```

<span data-ttu-id="ad399-114">To polecenie usuwa partnera kont integracyjnych o nazwie IntegrationAccountPartner1.</span><span class="sxs-lookup"><span data-stu-id="ad399-114">This command removes the integration account partner named IntegrationAccountPartner1.</span></span>

## <span data-ttu-id="ad399-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ad399-115">PARAMETERS</span></span>

### <span data-ttu-id="ad399-116">-Force</span><span class="sxs-lookup"><span data-stu-id="ad399-116">-Force</span></span>
<span data-ttu-id="ad399-117">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="ad399-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ad399-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ad399-118">-Name</span></span>
<span data-ttu-id="ad399-119">Określa nazwę konta integracji.</span><span class="sxs-lookup"><span data-stu-id="ad399-119">Specifies the name of an integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad399-120">-Partnername</span><span class="sxs-lookup"><span data-stu-id="ad399-120">-PartnerName</span></span>
<span data-ttu-id="ad399-121">Określa nazwę partnera kont integracji.</span><span class="sxs-lookup"><span data-stu-id="ad399-121">Specifies the name of the integration account partner.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad399-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad399-122">-ResourceGroupName</span></span>
<span data-ttu-id="ad399-123">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="ad399-123">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="ad399-124">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ad399-124">-Confirm</span></span>
<span data-ttu-id="ad399-125">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ad399-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ad399-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad399-126">-WhatIf</span></span>
<span data-ttu-id="ad399-127">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ad399-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ad399-128">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ad399-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ad399-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad399-129">-DefaultProfile</span></span>
<span data-ttu-id="ad399-130">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ad399-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ad399-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad399-131">CommonParameters</span></span>
<span data-ttu-id="ad399-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad399-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad399-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad399-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad399-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ad399-134">INPUTS</span></span>

## <span data-ttu-id="ad399-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ad399-135">OUTPUTS</span></span>

## <span data-ttu-id="ad399-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ad399-136">NOTES</span></span>

## <span data-ttu-id="ad399-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ad399-137">RELATED LINKS</span></span>

[<span data-ttu-id="ad399-138">Get-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="ad399-138">Get-AzureRmIntegrationAccountPartner</span></span>](./Get-AzureRmIntegrationAccountPartner.md)

[<span data-ttu-id="ad399-139">Nowe — AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="ad399-139">New-AzureRmIntegrationAccountPartner</span></span>](./New-AzureRmIntegrationAccountPartner.md)

[<span data-ttu-id="ad399-140">Set-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="ad399-140">Set-AzureRmIntegrationAccountPartner</span></span>](./Set-AzureRmIntegrationAccountPartner.md)


