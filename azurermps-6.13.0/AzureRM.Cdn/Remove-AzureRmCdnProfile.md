---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 3A4F8442-1268-44BC-91ED-47C03CD20C47
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/remove-azurermcdnprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Remove-AzureRmCdnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Remove-AzureRmCdnProfile.md
ms.openlocfilehash: 0c39e6ee26faffc9c12e2fc3b5f00ccaadfa9389
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93547524"
---
# <span data-ttu-id="1429f-101">Remove-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="1429f-101">Remove-AzureRmCdnProfile</span></span>

## <span data-ttu-id="1429f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1429f-102">SYNOPSIS</span></span>
<span data-ttu-id="1429f-103">Usuwa profil sieci CDN.</span><span class="sxs-lookup"><span data-stu-id="1429f-103">Removes a CDN profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1429f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1429f-104">SYNTAX</span></span>

### <span data-ttu-id="1429f-105">ByFieldsParameterSet</span><span class="sxs-lookup"><span data-stu-id="1429f-105">ByFieldsParameterSet</span></span>
```
Remove-AzureRmCdnProfile -ProfileName <String> -ResourceGroupName <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1429f-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1429f-106">ByObjectParameterSet</span></span>
```
Remove-AzureRmCdnProfile -CdnProfile <PSProfile> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1429f-107">Opis</span><span class="sxs-lookup"><span data-stu-id="1429f-107">DESCRIPTION</span></span>
<span data-ttu-id="1429f-108">Polecenie cmdlet **Remove-AzureRmCdnProfile** usuwa profil sieci dostarczania zawartości Azure (CDN, Content Delivery Network).</span><span class="sxs-lookup"><span data-stu-id="1429f-108">The **Remove-AzureRmCdnProfile** cmdlet removes a Azure Content Delivery Network (CDN) profile.</span></span>

## <span data-ttu-id="1429f-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1429f-109">EXAMPLES</span></span>

## <span data-ttu-id="1429f-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1429f-110">PARAMETERS</span></span>

### <span data-ttu-id="1429f-111">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="1429f-111">-CdnProfile</span></span>
<span data-ttu-id="1429f-112">Określa profil, który jest usuwany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1429f-112">Specifies the profile that this cmdlet removes.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1429f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1429f-113">-DefaultProfile</span></span>
<span data-ttu-id="1429f-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="1429f-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1429f-115">-Force</span><span class="sxs-lookup"><span data-stu-id="1429f-115">-Force</span></span>
<span data-ttu-id="1429f-116">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="1429f-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="1429f-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1429f-117">-PassThru</span></span>
<span data-ttu-id="1429f-118">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="1429f-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="1429f-119">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="1429f-119">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1429f-120">-Refilename</span><span class="sxs-lookup"><span data-stu-id="1429f-120">-ProfileName</span></span>
<span data-ttu-id="1429f-121">Określa nazwę profilu usuniętego przez ten aplet polecenia.</span><span class="sxs-lookup"><span data-stu-id="1429f-121">Specifies the name of the profile that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1429f-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1429f-122">-ResourceGroupName</span></span>
<span data-ttu-id="1429f-123">Określa nazwę grupy zasobów, do której należy profil.</span><span class="sxs-lookup"><span data-stu-id="1429f-123">Specifies the name of the resource group to which the profile belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1429f-124">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1429f-124">-Confirm</span></span>
<span data-ttu-id="1429f-125">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1429f-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1429f-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1429f-126">-WhatIf</span></span>
<span data-ttu-id="1429f-127">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1429f-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1429f-128">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="1429f-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1429f-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1429f-129">CommonParameters</span></span>
<span data-ttu-id="1429f-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1429f-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1429f-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1429f-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1429f-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1429f-132">INPUTS</span></span>

### <span data-ttu-id="1429f-133">Microsoft. Azure. Commands. CDN. models. profile. PSProfile</span><span class="sxs-lookup"><span data-stu-id="1429f-133">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>
<span data-ttu-id="1429f-134">Parametry: CdnProfile (ByValue)</span><span class="sxs-lookup"><span data-stu-id="1429f-134">Parameters: CdnProfile (ByValue)</span></span>

### <span data-ttu-id="1429f-135">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="1429f-135">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="1429f-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1429f-136">OUTPUTS</span></span>

### <span data-ttu-id="1429f-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1429f-137">System.Boolean</span></span>

## <span data-ttu-id="1429f-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1429f-138">NOTES</span></span>

## <span data-ttu-id="1429f-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1429f-139">RELATED LINKS</span></span>

[<span data-ttu-id="1429f-140">Get-AzureRMCdnProfile</span><span class="sxs-lookup"><span data-stu-id="1429f-140">Get-AzureRMCdnProfile</span></span>](./Get-AzureRMCdnProfile.md)

[<span data-ttu-id="1429f-141">Nowe — AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="1429f-141">New-AzureRmCdnProfile</span></span>](./New-AzureRmCdnProfile.md)

[<span data-ttu-id="1429f-142">Set-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="1429f-142">Set-AzureRmCdnProfile</span></span>](./Set-AzureRmCdnProfile.md)


