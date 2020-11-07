---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: EBDBB9F0-CA2E-4E4F-9034-3D0FAB88E442
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/remove-azintegrationaccountagreement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountAgreement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountAgreement.md
ms.openlocfilehash: d320d29a9c5e6136caafde2b7d355a6a2ebf9ca6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93705002"
---
# <span data-ttu-id="ad2f8-101">Remove-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="ad2f8-101">Remove-AzIntegrationAccountAgreement</span></span>

## <span data-ttu-id="ad2f8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ad2f8-102">SYNOPSIS</span></span>
<span data-ttu-id="ad2f8-103">Usuwa umowę dotyczącą konta integracji.</span><span class="sxs-lookup"><span data-stu-id="ad2f8-103">Removes an integration account agreement.</span></span>

## <span data-ttu-id="ad2f8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ad2f8-104">SYNTAX</span></span>

```
Remove-AzIntegrationAccountAgreement -ResourceGroupName <String> -Name <String> -AgreementName <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ad2f8-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ad2f8-105">DESCRIPTION</span></span>
<span data-ttu-id="ad2f8-106">Polecenie cmdlet **Remove-AzIntegrationAccountAgreement** usuwa umowę dotyczącą konta integracji z grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="ad2f8-106">The **Remove-AzIntegrationAccountAgreement** cmdlet removes an integration account agreement from an Azure resource group.</span></span>
<span data-ttu-id="ad2f8-107">Określ nazwę konta integracji, nazwę grupy zasobów i nazwę umowy.</span><span class="sxs-lookup"><span data-stu-id="ad2f8-107">Specify the integration account name, resource group name, and agreement name.</span></span>
<span data-ttu-id="ad2f8-108">Ten moduł obsługuje parametry dynamiczne.</span><span class="sxs-lookup"><span data-stu-id="ad2f8-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="ad2f8-109">Aby użyć parametru dynamicznego, wpisz go w poleceniu.</span><span class="sxs-lookup"><span data-stu-id="ad2f8-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="ad2f8-110">Aby wykryć nazwy parametrów dynamicznych, wpisz znak łącznika (-) po nazwie polecenia cmdlet, a następnie naciskaj klawisz Tab, aby przechodzić między dostępnymi parametrami.</span><span class="sxs-lookup"><span data-stu-id="ad2f8-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="ad2f8-111">W przypadku pominięcia wymaganego parametru szablonu polecenie cmdlet monituje o podanie wartości.</span><span class="sxs-lookup"><span data-stu-id="ad2f8-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="ad2f8-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ad2f8-112">EXAMPLES</span></span>

### <span data-ttu-id="ad2f8-113">Przykład 1: usuwanie umowy dotyczącej konta integracji według nazwy</span><span class="sxs-lookup"><span data-stu-id="ad2f8-113">Example 1: Remove an integration account agreement by name</span></span>
```
PS C:\>Remove-AzIntegrationAccountAgreement -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -AgreementName "IntegrationAccountAgreement06" -Force
```

<span data-ttu-id="ad2f8-114">To polecenie usuwa umowę dotyczącą konta integracji o nazwie IntegrationAccountAgreement06.</span><span class="sxs-lookup"><span data-stu-id="ad2f8-114">This command removes the integration account agreement named IntegrationAccountAgreement06.</span></span>
<span data-ttu-id="ad2f8-115">Polecenie nie wyświetla monitu o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="ad2f8-115">The command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="ad2f8-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ad2f8-116">PARAMETERS</span></span>

### <span data-ttu-id="ad2f8-117">-Agreementname</span><span class="sxs-lookup"><span data-stu-id="ad2f8-117">-AgreementName</span></span>
<span data-ttu-id="ad2f8-118">Określa nazwę umowy dotyczącej konta integracji.</span><span class="sxs-lookup"><span data-stu-id="ad2f8-118">Specifies the name of the integration account agreement.</span></span>

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

### <span data-ttu-id="ad2f8-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad2f8-119">-DefaultProfile</span></span>
<span data-ttu-id="ad2f8-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="ad2f8-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ad2f8-121">-Force</span><span class="sxs-lookup"><span data-stu-id="ad2f8-121">-Force</span></span>
<span data-ttu-id="ad2f8-122">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="ad2f8-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ad2f8-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ad2f8-123">-Name</span></span>
<span data-ttu-id="ad2f8-124">Określa nazwę konta integracji.</span><span class="sxs-lookup"><span data-stu-id="ad2f8-124">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="ad2f8-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad2f8-125">-ResourceGroupName</span></span>
<span data-ttu-id="ad2f8-126">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="ad2f8-126">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="ad2f8-127">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ad2f8-127">-Confirm</span></span>
<span data-ttu-id="ad2f8-128">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ad2f8-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ad2f8-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad2f8-129">-WhatIf</span></span>
<span data-ttu-id="ad2f8-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ad2f8-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ad2f8-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ad2f8-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ad2f8-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad2f8-132">CommonParameters</span></span>
<span data-ttu-id="ad2f8-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad2f8-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad2f8-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad2f8-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad2f8-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ad2f8-135">INPUTS</span></span>

### <span data-ttu-id="ad2f8-136">System. String</span><span class="sxs-lookup"><span data-stu-id="ad2f8-136">System.String</span></span>

## <span data-ttu-id="ad2f8-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ad2f8-137">OUTPUTS</span></span>

### <span data-ttu-id="ad2f8-138">System. void</span><span class="sxs-lookup"><span data-stu-id="ad2f8-138">System.Void</span></span>

## <span data-ttu-id="ad2f8-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ad2f8-139">NOTES</span></span>

## <span data-ttu-id="ad2f8-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ad2f8-140">RELATED LINKS</span></span>

[<span data-ttu-id="ad2f8-141">Get-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="ad2f8-141">Get-AzIntegrationAccountAgreement</span></span>](./Get-AzIntegrationAccountAgreement.md)

[<span data-ttu-id="ad2f8-142">Nowe — AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="ad2f8-142">New-AzIntegrationAccountAgreement</span></span>](./New-AzIntegrationAccountAgreement.md)

[<span data-ttu-id="ad2f8-143">Set-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="ad2f8-143">Set-AzIntegrationAccountAgreement</span></span>](./Set-AzIntegrationAccountAgreement.md)


