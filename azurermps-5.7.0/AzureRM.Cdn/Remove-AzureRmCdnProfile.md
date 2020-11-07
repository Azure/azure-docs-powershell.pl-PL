---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 3A4F8442-1268-44BC-91ED-47C03CD20C47
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/remove-azurermcdnprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Remove-AzureRmCdnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Remove-AzureRmCdnProfile.md
ms.openlocfilehash: 76c1f255b2d8dc3275ec3a691337019a7fd1e3e0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718959"
---
# <span data-ttu-id="02011-101">Remove-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="02011-101">Remove-AzureRmCdnProfile</span></span>

## <span data-ttu-id="02011-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="02011-102">SYNOPSIS</span></span>
<span data-ttu-id="02011-103">Usuwa profil sieci CDN.</span><span class="sxs-lookup"><span data-stu-id="02011-103">Removes a CDN profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="02011-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="02011-104">SYNTAX</span></span>

### <span data-ttu-id="02011-105">ByFieldsParameterSet</span><span class="sxs-lookup"><span data-stu-id="02011-105">ByFieldsParameterSet</span></span>
```
Remove-AzureRmCdnProfile -ProfileName <String> -ResourceGroupName <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="02011-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="02011-106">ByObjectParameterSet</span></span>
```
Remove-AzureRmCdnProfile -CdnProfile <PSProfile> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="02011-107">Opis</span><span class="sxs-lookup"><span data-stu-id="02011-107">DESCRIPTION</span></span>
<span data-ttu-id="02011-108">Polecenie cmdlet **Remove-AzureRmCdnProfile** usuwa profil sieci dostarczania zawartości Azure (CDN, Content Delivery Network).</span><span class="sxs-lookup"><span data-stu-id="02011-108">The **Remove-AzureRmCdnProfile** cmdlet removes a Azure Content Delivery Network (CDN) profile.</span></span>

## <span data-ttu-id="02011-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="02011-109">EXAMPLES</span></span>

## <span data-ttu-id="02011-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="02011-110">PARAMETERS</span></span>

### <span data-ttu-id="02011-111">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="02011-111">-CdnProfile</span></span>
<span data-ttu-id="02011-112">Określa profil, który jest usuwany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="02011-112">Specifies the profile that this cmdlet removes.</span></span>

```yaml
Type: PSProfile
Parameter Sets: ByObjectParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="02011-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02011-113">-DefaultProfile</span></span>
<span data-ttu-id="02011-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="02011-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="02011-115">-Force</span><span class="sxs-lookup"><span data-stu-id="02011-115">-Force</span></span>
<span data-ttu-id="02011-116">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="02011-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="02011-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="02011-117">-PassThru</span></span>
<span data-ttu-id="02011-118">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="02011-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="02011-119">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="02011-119">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02011-120">-Refilename</span><span class="sxs-lookup"><span data-stu-id="02011-120">-ProfileName</span></span>
<span data-ttu-id="02011-121">Określa nazwę profilu usuniętego przez ten aplet polecenia.</span><span class="sxs-lookup"><span data-stu-id="02011-121">Specifies the name of the profile that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02011-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02011-122">-ResourceGroupName</span></span>
<span data-ttu-id="02011-123">Określa nazwę grupy zasobów, do której należy profil.</span><span class="sxs-lookup"><span data-stu-id="02011-123">Specifies the name of the resource group to which the profile belongs.</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02011-124">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="02011-124">-Confirm</span></span>
<span data-ttu-id="02011-125">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="02011-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="02011-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02011-126">-WhatIf</span></span>
<span data-ttu-id="02011-127">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="02011-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="02011-128">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="02011-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="02011-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02011-129">CommonParameters</span></span>
<span data-ttu-id="02011-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="02011-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02011-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="02011-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02011-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="02011-132">INPUTS</span></span>

### <span data-ttu-id="02011-133">PSProfile</span><span class="sxs-lookup"><span data-stu-id="02011-133">PSProfile</span></span>
<span data-ttu-id="02011-134">Parametr "CdnProfile" akceptuje wartość typu "PSProfile" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="02011-134">Parameter 'CdnProfile' accepts value of type 'PSProfile' from the pipeline</span></span>

## <span data-ttu-id="02011-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="02011-135">OUTPUTS</span></span>

### <span data-ttu-id="02011-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="02011-136">System.Boolean</span></span>

## <span data-ttu-id="02011-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="02011-137">NOTES</span></span>

## <span data-ttu-id="02011-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="02011-138">RELATED LINKS</span></span>

[<span data-ttu-id="02011-139">Get-AzureRMCdnProfile</span><span class="sxs-lookup"><span data-stu-id="02011-139">Get-AzureRMCdnProfile</span></span>](./Get-AzureRMCdnProfile.md)

[<span data-ttu-id="02011-140">Nowe — AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="02011-140">New-AzureRmCdnProfile</span></span>](./New-AzureRmCdnProfile.md)

[<span data-ttu-id="02011-141">Set-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="02011-141">Set-AzureRmCdnProfile</span></span>](./Set-AzureRmCdnProfile.md)


