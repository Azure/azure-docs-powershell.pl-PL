---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: DDA137FD-4EB3-4FB7-A202-978922038AFC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/remove-azurermlogprofile
schema: 2.0.0
ms.openlocfilehash: 78d2bff42382564bb07f680b5db8db39707ffb97
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93897433"
---
# <span data-ttu-id="ce40e-101">Remove-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="ce40e-101">Remove-AzureRmLogProfile</span></span>

## <span data-ttu-id="ce40e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ce40e-102">SYNOPSIS</span></span>
<span data-ttu-id="ce40e-103">Usuwa profil dziennika.</span><span class="sxs-lookup"><span data-stu-id="ce40e-103">Removes a log profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ce40e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ce40e-104">SYNTAX</span></span>

```
Remove-AzureRmLogProfile -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ce40e-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ce40e-105">DESCRIPTION</span></span>
<span data-ttu-id="ce40e-106">Polecenie cmdlet **Remove-AzureRmLogProfile** usuwa profil dziennika.</span><span class="sxs-lookup"><span data-stu-id="ce40e-106">The **Remove-AzureRmLogProfile** cmdlet removes a log profile.</span></span>
<span data-ttu-id="ce40e-107">To polecenie cmdlet implementuje wzorzec ShouldProcess, tzn. może zażądać potwierdzenia od użytkownika przed faktycznym utworzeniem, zmodyfikowaniem lub usunięciem zasobu.</span><span class="sxs-lookup"><span data-stu-id="ce40e-107">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="ce40e-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ce40e-108">EXAMPLES</span></span>

## <span data-ttu-id="ce40e-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ce40e-109">PARAMETERS</span></span>

### <span data-ttu-id="ce40e-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce40e-110">-DefaultProfile</span></span>
<span data-ttu-id="ce40e-111">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="ce40e-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ce40e-112">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ce40e-112">-Name</span></span>
<span data-ttu-id="ce40e-113">Określa nazwę profilu dziennika, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="ce40e-113">Specifies the name of the log profile to remove.</span></span>

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

### <span data-ttu-id="ce40e-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ce40e-114">-PassThru</span></span>
<span data-ttu-id="ce40e-115">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="ce40e-115">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="ce40e-116">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ce40e-116">-Confirm</span></span>
<span data-ttu-id="ce40e-117">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ce40e-117">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce40e-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ce40e-118">-WhatIf</span></span>
<span data-ttu-id="ce40e-119">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ce40e-119">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ce40e-120">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ce40e-120">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce40e-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce40e-121">CommonParameters</span></span>
<span data-ttu-id="ce40e-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ce40e-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce40e-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ce40e-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce40e-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ce40e-124">INPUTS</span></span>

### <span data-ttu-id="ce40e-125">System. String</span><span class="sxs-lookup"><span data-stu-id="ce40e-125">System.String</span></span>

## <span data-ttu-id="ce40e-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ce40e-126">OUTPUTS</span></span>

### <span data-ttu-id="ce40e-127">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="ce40e-127">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="ce40e-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ce40e-128">NOTES</span></span>

## <span data-ttu-id="ce40e-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ce40e-129">RELATED LINKS</span></span>

[<span data-ttu-id="ce40e-130">Dodaj-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="ce40e-130">Add-AzureRmLogProfile</span></span>](./Add-AzureRmLogProfile.md)

[<span data-ttu-id="ce40e-131">Get-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="ce40e-131">Get-AzureRmLogProfile</span></span>](./Get-AzureRmLogProfile.md)


