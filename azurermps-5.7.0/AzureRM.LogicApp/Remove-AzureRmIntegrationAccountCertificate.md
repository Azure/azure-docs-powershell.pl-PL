---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: F9871519-F470-470C-8CCE-A674B6B5A3EE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/remove-azurermintegrationaccountcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Remove-AzureRmIntegrationAccountCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Remove-AzureRmIntegrationAccountCertificate.md
ms.openlocfilehash: 24d12f0ce75b38c56be3bff5a86694f032052b33
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528110"
---
# <span data-ttu-id="7b3ff-101">Remove-AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="7b3ff-101">Remove-AzureRmIntegrationAccountCertificate</span></span>

## <span data-ttu-id="7b3ff-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7b3ff-102">SYNOPSIS</span></span>
<span data-ttu-id="7b3ff-103">Usuwa certyfikat konta integracyjnego z grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="7b3ff-103">Removes an integration account certificate from a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7b3ff-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7b3ff-104">SYNTAX</span></span>

```
Remove-AzureRmIntegrationAccountCertificate -ResourceGroupName <String> -Name <String>
 -CertificateName <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7b3ff-105">Opis</span><span class="sxs-lookup"><span data-stu-id="7b3ff-105">DESCRIPTION</span></span>
<span data-ttu-id="7b3ff-106">Polecenie cmdlet **Remove-AzureRmIntegrationAccountCertificate** usuwa certyfikat konta integracyjnego z grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="7b3ff-106">The **Remove-AzureRmIntegrationAccountCertificate** cmdlet removes an integration account certificate from a resource group.</span></span>
<span data-ttu-id="7b3ff-107">Określ nazwę konta integracji, nazwę grupy zasobów i nazwę certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="7b3ff-107">Specify the integration account name, resource group name, and certificate name.</span></span>

<span data-ttu-id="7b3ff-108">Ten moduł obsługuje parametry dynamiczne.</span><span class="sxs-lookup"><span data-stu-id="7b3ff-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="7b3ff-109">Aby użyć parametru dynamicznego, wpisz go w poleceniu.</span><span class="sxs-lookup"><span data-stu-id="7b3ff-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="7b3ff-110">Aby wykryć nazwy parametrów dynamicznych, wpisz znak łącznika (-) po nazwie polecenia cmdlet, a następnie naciskaj klawisz Tab, aby przechodzić między dostępnymi parametrami.</span><span class="sxs-lookup"><span data-stu-id="7b3ff-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="7b3ff-111">W przypadku pominięcia wymaganego parametru szablonu polecenie cmdlet monituje o podanie wartości.</span><span class="sxs-lookup"><span data-stu-id="7b3ff-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="7b3ff-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7b3ff-112">EXAMPLES</span></span>

### <span data-ttu-id="7b3ff-113">Przykład 1: Usuwanie certyfikatu konta integracji</span><span class="sxs-lookup"><span data-stu-id="7b3ff-113">Example 1: Remove an integration account certificate</span></span>
```
PS C:\>Remove-AzureRmIntegrationAccountCertificate -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -CertificateName "IntegrationAccountCertificate01"
```

<span data-ttu-id="7b3ff-114">To polecenie usuwa certyfikat konta integracyjnego o nazwie IntegrationAccount31.</span><span class="sxs-lookup"><span data-stu-id="7b3ff-114">This command removes the integration account certificate named IntegrationAccount31.</span></span>

## <span data-ttu-id="7b3ff-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7b3ff-115">PARAMETERS</span></span>

### <span data-ttu-id="7b3ff-116">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="7b3ff-116">-CertificateName</span></span>
<span data-ttu-id="7b3ff-117">Określa nazwę certyfikatu konta integracyjnego.</span><span class="sxs-lookup"><span data-stu-id="7b3ff-117">Specifies the name of an integration account certificate.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b3ff-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b3ff-118">-DefaultProfile</span></span>
<span data-ttu-id="7b3ff-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="7b3ff-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b3ff-120">-Force</span><span class="sxs-lookup"><span data-stu-id="7b3ff-120">-Force</span></span>
<span data-ttu-id="7b3ff-121">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="7b3ff-121">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b3ff-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="7b3ff-122">-Name</span></span>
<span data-ttu-id="7b3ff-123">Określa nazwę konta integracji.</span><span class="sxs-lookup"><span data-stu-id="7b3ff-123">Specifies the name of an integration account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b3ff-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7b3ff-124">-ResourceGroupName</span></span>
<span data-ttu-id="7b3ff-125">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="7b3ff-125">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b3ff-126">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7b3ff-126">-Confirm</span></span>
<span data-ttu-id="7b3ff-127">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7b3ff-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b3ff-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7b3ff-128">-WhatIf</span></span>
<span data-ttu-id="7b3ff-129">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7b3ff-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7b3ff-130">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="7b3ff-130">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b3ff-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b3ff-131">CommonParameters</span></span>
<span data-ttu-id="7b3ff-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7b3ff-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b3ff-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7b3ff-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b3ff-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7b3ff-134">INPUTS</span></span>

### <span data-ttu-id="7b3ff-135">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="7b3ff-135">None</span></span>
<span data-ttu-id="7b3ff-136">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="7b3ff-136">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="7b3ff-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7b3ff-137">OUTPUTS</span></span>

## <span data-ttu-id="7b3ff-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7b3ff-138">NOTES</span></span>

## <span data-ttu-id="7b3ff-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7b3ff-139">RELATED LINKS</span></span>

[<span data-ttu-id="7b3ff-140">Get-AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="7b3ff-140">Get-AzureRmIntegrationAccountCertificate</span></span>](./Get-AzureRmIntegrationAccountCertificate.md)

[<span data-ttu-id="7b3ff-141">Nowe — AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="7b3ff-141">New-AzureRmIntegrationAccountCertificate</span></span>](./New-AzureRmIntegrationAccountCertificate.md)

[<span data-ttu-id="7b3ff-142">Set-AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="7b3ff-142">Set-AzureRmIntegrationAccountCertificate</span></span>](./Set-AzureRmIntegrationAccountCertificate.md)


