---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: EBDBB9F0-CA2E-4E4F-9034-3D0FAB88E442
online version: https://docs.microsoft.com/powershell/module/az.logicapp/remove-azintegrationaccountagreement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountAgreement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountAgreement.md
ms.openlocfilehash: cd15a6f132360bba973e9361cf2f6e98c9bf24f8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101968938"
---
# <span data-ttu-id="229fd-101">Remove-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="229fd-101">Remove-AzIntegrationAccountAgreement</span></span>

## <span data-ttu-id="229fd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="229fd-102">SYNOPSIS</span></span>
<span data-ttu-id="229fd-103">Usuwa umowę na konto integracji.</span><span class="sxs-lookup"><span data-stu-id="229fd-103">Removes an integration account agreement.</span></span>

## <span data-ttu-id="229fd-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="229fd-104">SYNTAX</span></span>

```
Remove-AzIntegrationAccountAgreement -ResourceGroupName <String> -Name <String> -AgreementName <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="229fd-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="229fd-105">DESCRIPTION</span></span>
<span data-ttu-id="229fd-106">Polecenie **cmdlet Remove-AzIntegrationAccountAgreement** usuwa umowę na konto integracji z grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="229fd-106">The **Remove-AzIntegrationAccountAgreement** cmdlet removes an integration account agreement from an Azure resource group.</span></span>
<span data-ttu-id="229fd-107">Określ nazwę konta integracji, nazwę grupy zasobów i nazwę umowy.</span><span class="sxs-lookup"><span data-stu-id="229fd-107">Specify the integration account name, resource group name, and agreement name.</span></span>
<span data-ttu-id="229fd-108">Ten moduł obsługuje parametry dynamiczne.</span><span class="sxs-lookup"><span data-stu-id="229fd-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="229fd-109">Aby użyć parametru dynamicznego, wpisz go w poleceniu.</span><span class="sxs-lookup"><span data-stu-id="229fd-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="229fd-110">Aby wykryć nazwy parametrów dynamicznych, wpisz łącznik (-) po nazwie polecenia cmdlet, a następnie naciskaj klawisz Tab, aby przechodzić przez dostępne parametry.</span><span class="sxs-lookup"><span data-stu-id="229fd-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="229fd-111">Jeśli pominiesz wymagany parametr szablonu, polecenie cmdlet wyświetli monit o wartość.</span><span class="sxs-lookup"><span data-stu-id="229fd-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="229fd-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="229fd-112">EXAMPLES</span></span>

### <span data-ttu-id="229fd-113">Przykład 1. Usunięcie umowy konta integracji według nazwy</span><span class="sxs-lookup"><span data-stu-id="229fd-113">Example 1: Remove an integration account agreement by name</span></span>
```
PS C:\>Remove-AzIntegrationAccountAgreement -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -AgreementName "IntegrationAccountAgreement06" -Force
```

<span data-ttu-id="229fd-114">To polecenie usuwa umowę o nazwie IntegrationAccountAgreement06 dla konta integracji.</span><span class="sxs-lookup"><span data-stu-id="229fd-114">This command removes the integration account agreement named IntegrationAccountAgreement06.</span></span>
<span data-ttu-id="229fd-115">To polecenie nie wyświetla monitu o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="229fd-115">The command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="229fd-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="229fd-116">PARAMETERS</span></span>

### <span data-ttu-id="229fd-117">-AgreementName</span><span class="sxs-lookup"><span data-stu-id="229fd-117">-AgreementName</span></span>
<span data-ttu-id="229fd-118">Określa nazwę umowy konta integracji.</span><span class="sxs-lookup"><span data-stu-id="229fd-118">Specifies the name of the integration account agreement.</span></span>

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

### <span data-ttu-id="229fd-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="229fd-119">-DefaultProfile</span></span>
<span data-ttu-id="229fd-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="229fd-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="229fd-121">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="229fd-121">-Force</span></span>
<span data-ttu-id="229fd-122">Wymusza uruchomienie polecenia bez pytania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="229fd-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="229fd-123">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="229fd-123">-Name</span></span>
<span data-ttu-id="229fd-124">Określa nazwę konta integracji.</span><span class="sxs-lookup"><span data-stu-id="229fd-124">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="229fd-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="229fd-125">-ResourceGroupName</span></span>
<span data-ttu-id="229fd-126">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="229fd-126">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="229fd-127">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="229fd-127">-Confirm</span></span>
<span data-ttu-id="229fd-128">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="229fd-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="229fd-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="229fd-129">-WhatIf</span></span>
<span data-ttu-id="229fd-130">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="229fd-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="229fd-131">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="229fd-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="229fd-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="229fd-132">CommonParameters</span></span>
<span data-ttu-id="229fd-133">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="229fd-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="229fd-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="229fd-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="229fd-135">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="229fd-135">INPUTS</span></span>

### <span data-ttu-id="229fd-136">System.String</span><span class="sxs-lookup"><span data-stu-id="229fd-136">System.String</span></span>

## <span data-ttu-id="229fd-137">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="229fd-137">OUTPUTS</span></span>

### <span data-ttu-id="229fd-138">System.Void</span><span class="sxs-lookup"><span data-stu-id="229fd-138">System.Void</span></span>

## <span data-ttu-id="229fd-139">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="229fd-139">NOTES</span></span>

## <span data-ttu-id="229fd-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="229fd-140">RELATED LINKS</span></span>

[<span data-ttu-id="229fd-141">Get-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="229fd-141">Get-AzIntegrationAccountAgreement</span></span>](./Get-AzIntegrationAccountAgreement.md)

[<span data-ttu-id="229fd-142">New-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="229fd-142">New-AzIntegrationAccountAgreement</span></span>](./New-AzIntegrationAccountAgreement.md)

[<span data-ttu-id="229fd-143">Set-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="229fd-143">Set-AzIntegrationAccountAgreement</span></span>](./Set-AzIntegrationAccountAgreement.md)


