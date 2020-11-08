---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: F9871519-F470-470C-8CCE-A674B6B5A3EE
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/remove-azintegrationaccountcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountCertificate.md
ms.openlocfilehash: 78bf9f5e61a66aee6c34dbeb7002d4b2e88e3b68
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94220782"
---
# <span data-ttu-id="b34ea-101">Remove-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="b34ea-101">Remove-AzIntegrationAccountCertificate</span></span>

## <span data-ttu-id="b34ea-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b34ea-102">SYNOPSIS</span></span>
<span data-ttu-id="b34ea-103">Usuwa certyfikat konta integracyjnego z grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b34ea-103">Removes an integration account certificate from a resource group.</span></span>

## <span data-ttu-id="b34ea-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b34ea-104">SYNTAX</span></span>

```
Remove-AzIntegrationAccountCertificate -ResourceGroupName <String> -Name <String> -CertificateName <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b34ea-105">Opis</span><span class="sxs-lookup"><span data-stu-id="b34ea-105">DESCRIPTION</span></span>
<span data-ttu-id="b34ea-106">Polecenie cmdlet **Remove-AzIntegrationAccountCertificate** usuwa certyfikat konta integracyjnego z grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b34ea-106">The **Remove-AzIntegrationAccountCertificate** cmdlet removes an integration account certificate from a resource group.</span></span>
<span data-ttu-id="b34ea-107">Określ nazwę konta integracji, nazwę grupy zasobów i nazwę certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="b34ea-107">Specify the integration account name, resource group name, and certificate name.</span></span>
<span data-ttu-id="b34ea-108">Ten moduł obsługuje parametry dynamiczne.</span><span class="sxs-lookup"><span data-stu-id="b34ea-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="b34ea-109">Aby użyć parametru dynamicznego, wpisz go w poleceniu.</span><span class="sxs-lookup"><span data-stu-id="b34ea-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="b34ea-110">Aby wykryć nazwy parametrów dynamicznych, wpisz znak łącznika (-) po nazwie polecenia cmdlet, a następnie naciskaj klawisz Tab, aby przechodzić między dostępnymi parametrami.</span><span class="sxs-lookup"><span data-stu-id="b34ea-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="b34ea-111">W przypadku pominięcia wymaganego parametru szablonu polecenie cmdlet monituje o podanie wartości.</span><span class="sxs-lookup"><span data-stu-id="b34ea-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="b34ea-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b34ea-112">EXAMPLES</span></span>

### <span data-ttu-id="b34ea-113">Przykład 1: Usuwanie certyfikatu konta integracji</span><span class="sxs-lookup"><span data-stu-id="b34ea-113">Example 1: Remove an integration account certificate</span></span>
```
PS C:\>Remove-AzIntegrationAccountCertificate -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -CertificateName "IntegrationAccountCertificate01"
```

<span data-ttu-id="b34ea-114">To polecenie usuwa certyfikat konta integracyjnego o nazwie IntegrationAccount31.</span><span class="sxs-lookup"><span data-stu-id="b34ea-114">This command removes the integration account certificate named IntegrationAccount31.</span></span>

## <span data-ttu-id="b34ea-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b34ea-115">PARAMETERS</span></span>

### <span data-ttu-id="b34ea-116">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="b34ea-116">-CertificateName</span></span>
<span data-ttu-id="b34ea-117">Określa nazwę certyfikatu konta integracyjnego.</span><span class="sxs-lookup"><span data-stu-id="b34ea-117">Specifies the name of an integration account certificate.</span></span>

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

### <span data-ttu-id="b34ea-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b34ea-118">-DefaultProfile</span></span>
<span data-ttu-id="b34ea-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="b34ea-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b34ea-120">-Force</span><span class="sxs-lookup"><span data-stu-id="b34ea-120">-Force</span></span>
<span data-ttu-id="b34ea-121">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="b34ea-121">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b34ea-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b34ea-122">-Name</span></span>
<span data-ttu-id="b34ea-123">Określa nazwę konta integracji.</span><span class="sxs-lookup"><span data-stu-id="b34ea-123">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="b34ea-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b34ea-124">-ResourceGroupName</span></span>
<span data-ttu-id="b34ea-125">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b34ea-125">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="b34ea-126">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b34ea-126">-Confirm</span></span>
<span data-ttu-id="b34ea-127">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b34ea-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b34ea-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b34ea-128">-WhatIf</span></span>
<span data-ttu-id="b34ea-129">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b34ea-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b34ea-130">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b34ea-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b34ea-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b34ea-131">CommonParameters</span></span>
<span data-ttu-id="b34ea-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b34ea-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b34ea-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b34ea-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b34ea-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b34ea-134">INPUTS</span></span>

### <span data-ttu-id="b34ea-135">System. String</span><span class="sxs-lookup"><span data-stu-id="b34ea-135">System.String</span></span>

## <span data-ttu-id="b34ea-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b34ea-136">OUTPUTS</span></span>

### <span data-ttu-id="b34ea-137">System. void</span><span class="sxs-lookup"><span data-stu-id="b34ea-137">System.Void</span></span>

## <span data-ttu-id="b34ea-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b34ea-138">NOTES</span></span>

## <span data-ttu-id="b34ea-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b34ea-139">RELATED LINKS</span></span>

[<span data-ttu-id="b34ea-140">Get-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="b34ea-140">Get-AzIntegrationAccountCertificate</span></span>](./Get-AzIntegrationAccountCertificate.md)

[<span data-ttu-id="b34ea-141">Nowe — AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="b34ea-141">New-AzIntegrationAccountCertificate</span></span>](./New-AzIntegrationAccountCertificate.md)

[<span data-ttu-id="b34ea-142">Set-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="b34ea-142">Set-AzIntegrationAccountCertificate</span></span>](./Set-AzIntegrationAccountCertificate.md)


