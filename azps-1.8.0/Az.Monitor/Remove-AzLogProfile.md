---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: DDA137FD-4EB3-4FB7-A202-978922038AFC
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/remove-azlogprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzLogProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzLogProfile.md
ms.openlocfilehash: 6b011201dec1c5ef7fd06f503843f7336f5ab220
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93709758"
---
# <span data-ttu-id="8bc64-101">Remove-AzLogProfile</span><span class="sxs-lookup"><span data-stu-id="8bc64-101">Remove-AzLogProfile</span></span>

## <span data-ttu-id="8bc64-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8bc64-102">SYNOPSIS</span></span>
<span data-ttu-id="8bc64-103">Usuwa profil dziennika.</span><span class="sxs-lookup"><span data-stu-id="8bc64-103">Removes a log profile.</span></span>

## <span data-ttu-id="8bc64-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8bc64-104">SYNTAX</span></span>

```
Remove-AzLogProfile -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8bc64-105">Opis</span><span class="sxs-lookup"><span data-stu-id="8bc64-105">DESCRIPTION</span></span>
<span data-ttu-id="8bc64-106">Polecenie cmdlet **Remove-AzLogProfile** usuwa profil dziennika.</span><span class="sxs-lookup"><span data-stu-id="8bc64-106">The **Remove-AzLogProfile** cmdlet removes a log profile.</span></span>
<span data-ttu-id="8bc64-107">To polecenie cmdlet implementuje wzorzec ShouldProcess, tzn. może zażądać potwierdzenia od użytkownika przed faktycznym utworzeniem, zmodyfikowaniem lub usunięciem zasobu.</span><span class="sxs-lookup"><span data-stu-id="8bc64-107">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="8bc64-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8bc64-108">EXAMPLES</span></span>

## <span data-ttu-id="8bc64-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8bc64-109">PARAMETERS</span></span>

### <span data-ttu-id="8bc64-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8bc64-110">-DefaultProfile</span></span>
<span data-ttu-id="8bc64-111">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="8bc64-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8bc64-112">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="8bc64-112">-Name</span></span>
<span data-ttu-id="8bc64-113">Określa nazwę profilu dziennika, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="8bc64-113">Specifies the name of the log profile to remove.</span></span>

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

### <span data-ttu-id="8bc64-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8bc64-114">-PassThru</span></span>
<span data-ttu-id="8bc64-115">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="8bc64-115">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="8bc64-116">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8bc64-116">-Confirm</span></span>
<span data-ttu-id="8bc64-117">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8bc64-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8bc64-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8bc64-118">-WhatIf</span></span>
<span data-ttu-id="8bc64-119">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8bc64-119">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8bc64-120">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="8bc64-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8bc64-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8bc64-121">CommonParameters</span></span>
<span data-ttu-id="8bc64-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8bc64-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8bc64-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8bc64-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8bc64-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8bc64-124">INPUTS</span></span>

### <span data-ttu-id="8bc64-125">System. String</span><span class="sxs-lookup"><span data-stu-id="8bc64-125">System.String</span></span>

## <span data-ttu-id="8bc64-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8bc64-126">OUTPUTS</span></span>

### <span data-ttu-id="8bc64-127">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="8bc64-127">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="8bc64-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8bc64-128">NOTES</span></span>

## <span data-ttu-id="8bc64-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8bc64-129">RELATED LINKS</span></span>

[<span data-ttu-id="8bc64-130">Dodaj-AzLogProfile</span><span class="sxs-lookup"><span data-stu-id="8bc64-130">Add-AzLogProfile</span></span>](./Add-AzLogProfile.md)

[<span data-ttu-id="8bc64-131">Get-AzLogProfile</span><span class="sxs-lookup"><span data-stu-id="8bc64-131">Get-AzLogProfile</span></span>](./Get-AzLogProfile.md)

