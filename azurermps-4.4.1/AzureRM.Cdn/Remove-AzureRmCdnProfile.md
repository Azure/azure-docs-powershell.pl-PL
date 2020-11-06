---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 3A4F8442-1268-44BC-91ED-47C03CD20C47
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Remove-AzureRmCdnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Remove-AzureRmCdnProfile.md
ms.openlocfilehash: f564a026359042a20e5d82e34425e98f1021422b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93547020"
---
# <span data-ttu-id="97837-101">Remove-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="97837-101">Remove-AzureRmCdnProfile</span></span>

## <span data-ttu-id="97837-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="97837-102">SYNOPSIS</span></span>
<span data-ttu-id="97837-103">Usuwa profil sieci CDN.</span><span class="sxs-lookup"><span data-stu-id="97837-103">Removes a CDN profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="97837-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="97837-104">SYNTAX</span></span>

### <span data-ttu-id="97837-105">Zestaw parametrów dla parametrów pól</span><span class="sxs-lookup"><span data-stu-id="97837-105">Parameter Set for fields parameters</span></span>
```
Remove-AzureRmCdnProfile -ProfileName <String> -ResourceGroupName <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="97837-106">Zestaw parametrów dla parametrów obiektu</span><span class="sxs-lookup"><span data-stu-id="97837-106">Parameter Set for object parameters</span></span>
```
Remove-AzureRmCdnProfile -CdnProfile <PSProfile> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="97837-107">Opis</span><span class="sxs-lookup"><span data-stu-id="97837-107">DESCRIPTION</span></span>
<span data-ttu-id="97837-108">Polecenie cmdlet **Remove-AzureRmCdnProfile** usuwa profil sieci dostarczania zawartości Azure (CDN, Content Delivery Network).</span><span class="sxs-lookup"><span data-stu-id="97837-108">The **Remove-AzureRmCdnProfile** cmdlet removes a Azure Content Delivery Network (CDN) profile.</span></span>

## <span data-ttu-id="97837-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="97837-109">EXAMPLES</span></span>

## <span data-ttu-id="97837-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="97837-110">PARAMETERS</span></span>

### <span data-ttu-id="97837-111">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="97837-111">-CdnProfile</span></span>
<span data-ttu-id="97837-112">Określa profil, który jest usuwany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="97837-112">Specifies the profile that this cmdlet removes.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile
Parameter Sets: Parameter Set for object parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="97837-113">-Force</span><span class="sxs-lookup"><span data-stu-id="97837-113">-Force</span></span>
<span data-ttu-id="97837-114">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="97837-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="97837-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="97837-115">-PassThru</span></span>
<span data-ttu-id="97837-116">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="97837-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="97837-117">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="97837-117">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="97837-118">-Refilename</span><span class="sxs-lookup"><span data-stu-id="97837-118">-ProfileName</span></span>
<span data-ttu-id="97837-119">Określa nazwę profilu usuniętego przez ten aplet polecenia.</span><span class="sxs-lookup"><span data-stu-id="97837-119">Specifies the name of the profile that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97837-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="97837-120">-ResourceGroupName</span></span>
<span data-ttu-id="97837-121">Określa nazwę grupy zasobów, do której należy profil.</span><span class="sxs-lookup"><span data-stu-id="97837-121">Specifies the name of the resource group to which the profile belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97837-122">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="97837-122">-Confirm</span></span>
<span data-ttu-id="97837-123">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="97837-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="97837-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="97837-124">-WhatIf</span></span>
<span data-ttu-id="97837-125">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="97837-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="97837-126">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="97837-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="97837-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97837-127">-DefaultProfile</span></span>
<span data-ttu-id="97837-128">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="97837-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="97837-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97837-129">CommonParameters</span></span>
<span data-ttu-id="97837-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97837-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97837-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="97837-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97837-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="97837-132">INPUTS</span></span>

### <span data-ttu-id="97837-133">PSProfile</span><span class="sxs-lookup"><span data-stu-id="97837-133">PSProfile</span></span>
<span data-ttu-id="97837-134">Parametr "CdnProfile" akceptuje wartość typu "PSProfile" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="97837-134">Parameter 'CdnProfile' accepts value of type 'PSProfile' from the pipeline</span></span>

## <span data-ttu-id="97837-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="97837-135">OUTPUTS</span></span>

### <span data-ttu-id="97837-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="97837-136">System.Boolean</span></span>

## <span data-ttu-id="97837-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="97837-137">NOTES</span></span>

## <span data-ttu-id="97837-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="97837-138">RELATED LINKS</span></span>

[<span data-ttu-id="97837-139">Get-AzureRMCdnProfile</span><span class="sxs-lookup"><span data-stu-id="97837-139">Get-AzureRMCdnProfile</span></span>](./Get-AzureRMCdnProfile.md)

[<span data-ttu-id="97837-140">Nowe — AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="97837-140">New-AzureRmCdnProfile</span></span>](./New-AzureRmCdnProfile.md)

[<span data-ttu-id="97837-141">Set-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="97837-141">Set-AzureRmCdnProfile</span></span>](./Set-AzureRmCdnProfile.md)


