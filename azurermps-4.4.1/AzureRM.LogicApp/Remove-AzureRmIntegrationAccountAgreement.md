---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: EBDBB9F0-CA2E-4E4F-9034-3D0FAB88E442
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Remove-AzureRmIntegrationAccountAgreement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Remove-AzureRmIntegrationAccountAgreement.md
ms.openlocfilehash: 63241b764576e06166e293f17717b26c4dcbe3d8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93549987"
---
# <span data-ttu-id="7c2ce-101">Remove-AzureRmIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="7c2ce-101">Remove-AzureRmIntegrationAccountAgreement</span></span>

## <span data-ttu-id="7c2ce-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7c2ce-102">SYNOPSIS</span></span>
<span data-ttu-id="7c2ce-103">Usuwa umowę dotyczącą konta integracji.</span><span class="sxs-lookup"><span data-stu-id="7c2ce-103">Removes an integration account agreement.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7c2ce-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7c2ce-104">SYNTAX</span></span>

```
Remove-AzureRmIntegrationAccountAgreement -ResourceGroupName <String> -Name <String> -AgreementName <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7c2ce-105">Opis</span><span class="sxs-lookup"><span data-stu-id="7c2ce-105">DESCRIPTION</span></span>
<span data-ttu-id="7c2ce-106">Polecenie cmdlet **Remove-AzureRmIntegrationAccountAgreement** usuwa umowę dotyczącą konta integracji z grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="7c2ce-106">The **Remove-AzureRmIntegrationAccountAgreement** cmdlet removes an integration account agreement from an Azure resource group.</span></span>
<span data-ttu-id="7c2ce-107">Określ nazwę konta integracji, nazwę grupy zasobów i nazwę umowy.</span><span class="sxs-lookup"><span data-stu-id="7c2ce-107">Specify the integration account name, resource group name, and agreement name.</span></span>

<span data-ttu-id="7c2ce-108">Ten moduł obsługuje parametry dynamiczne.</span><span class="sxs-lookup"><span data-stu-id="7c2ce-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="7c2ce-109">Aby użyć parametru dynamicznego, wpisz go w poleceniu.</span><span class="sxs-lookup"><span data-stu-id="7c2ce-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="7c2ce-110">Aby wykryć nazwy parametrów dynamicznych, wpisz znak łącznika (-) po nazwie polecenia cmdlet, a następnie naciskaj klawisz Tab, aby przechodzić między dostępnymi parametrami.</span><span class="sxs-lookup"><span data-stu-id="7c2ce-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="7c2ce-111">W przypadku pominięcia wymaganego parametru szablonu polecenie cmdlet monituje o podanie wartości.</span><span class="sxs-lookup"><span data-stu-id="7c2ce-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="7c2ce-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7c2ce-112">EXAMPLES</span></span>

### <span data-ttu-id="7c2ce-113">Przykład 1: usuwanie umowy dotyczącej konta integracji według nazwy</span><span class="sxs-lookup"><span data-stu-id="7c2ce-113">Example 1: Remove an integration account agreement by name</span></span>
```
PS C:\>Remove-AzureRmIntegrationAccountAgreement -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -AgreementName "IntegrationAccountAgreement06" -Force
```

<span data-ttu-id="7c2ce-114">To polecenie usuwa umowę dotyczącą konta integracji o nazwie IntegrationAccountAgreement06.</span><span class="sxs-lookup"><span data-stu-id="7c2ce-114">This command removes the integration account agreement named IntegrationAccountAgreement06.</span></span>
<span data-ttu-id="7c2ce-115">Polecenie nie wyświetla monitu o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="7c2ce-115">The command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="7c2ce-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7c2ce-116">PARAMETERS</span></span>

### <span data-ttu-id="7c2ce-117">-Agreementname</span><span class="sxs-lookup"><span data-stu-id="7c2ce-117">-AgreementName</span></span>
<span data-ttu-id="7c2ce-118">Określa nazwę umowy dotyczącej konta integracji.</span><span class="sxs-lookup"><span data-stu-id="7c2ce-118">Specifies the name of the integration account agreement.</span></span>

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

### <span data-ttu-id="7c2ce-119">-Force</span><span class="sxs-lookup"><span data-stu-id="7c2ce-119">-Force</span></span>
<span data-ttu-id="7c2ce-120">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="7c2ce-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="7c2ce-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="7c2ce-121">-Name</span></span>
<span data-ttu-id="7c2ce-122">Określa nazwę konta integracji.</span><span class="sxs-lookup"><span data-stu-id="7c2ce-122">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="7c2ce-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c2ce-123">-ResourceGroupName</span></span>
<span data-ttu-id="7c2ce-124">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="7c2ce-124">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="7c2ce-125">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7c2ce-125">-Confirm</span></span>
<span data-ttu-id="7c2ce-126">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7c2ce-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7c2ce-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7c2ce-127">-WhatIf</span></span>
<span data-ttu-id="7c2ce-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7c2ce-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7c2ce-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="7c2ce-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7c2ce-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c2ce-130">-DefaultProfile</span></span>
<span data-ttu-id="7c2ce-131">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7c2ce-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7c2ce-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c2ce-132">CommonParameters</span></span>
<span data-ttu-id="7c2ce-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7c2ce-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c2ce-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7c2ce-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c2ce-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7c2ce-135">INPUTS</span></span>

## <span data-ttu-id="7c2ce-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7c2ce-136">OUTPUTS</span></span>

## <span data-ttu-id="7c2ce-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7c2ce-137">NOTES</span></span>

## <span data-ttu-id="7c2ce-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7c2ce-138">RELATED LINKS</span></span>

[<span data-ttu-id="7c2ce-139">Get-AzureRmIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="7c2ce-139">Get-AzureRmIntegrationAccountAgreement</span></span>](./Get-AzureRmIntegrationAccountAgreement.md)

[<span data-ttu-id="7c2ce-140">Nowe — AzureRmIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="7c2ce-140">New-AzureRmIntegrationAccountAgreement</span></span>](./New-AzureRmIntegrationAccountAgreement.md)

[<span data-ttu-id="7c2ce-141">Set-AzureRmIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="7c2ce-141">Set-AzureRmIntegrationAccountAgreement</span></span>](./Set-AzureRmIntegrationAccountAgreement.md)


