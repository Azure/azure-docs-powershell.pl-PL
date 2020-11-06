---
external help file: Microsoft.Azure.Commands.RecoveryServices.ARM.dll-Help.xml
Module Name: AzureRM.RecoveryServices
ms.assetid: 9591E150-54DA-48B7-8656-3891833FE61E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/New-AzureRmRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/New-AzureRmRecoveryServicesVault.md
ms.openlocfilehash: d9163e42b199dd5178e37a7d1bbe22abbb05c7f6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527345"
---
# <span data-ttu-id="604de-101">New-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="604de-101">New-AzureRmRecoveryServicesVault</span></span>

## <span data-ttu-id="604de-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="604de-102">SYNOPSIS</span></span>
<span data-ttu-id="604de-103">Tworzy nowy magazyn usług Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="604de-103">Creates a new Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="604de-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="604de-104">SYNTAX</span></span>

```
New-AzureRmRecoveryServicesVault -Name <String> -ResourceGroupName <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="604de-105">Opis</span><span class="sxs-lookup"><span data-stu-id="604de-105">DESCRIPTION</span></span>
<span data-ttu-id="604de-106">Polecenie cmdlet **New-AzureRmRecoveryServicesVault** tworzy nowy magazyn usług Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="604de-106">The **New-AzureRmRecoveryServicesVault** cmdlet creates a new Recovery Services vault.</span></span>

## <span data-ttu-id="604de-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="604de-107">EXAMPLES</span></span>

## <span data-ttu-id="604de-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="604de-108">PARAMETERS</span></span>

### <span data-ttu-id="604de-109">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="604de-109">-Location</span></span>
<span data-ttu-id="604de-110">Określa nazwę lokalizacji geograficznej magazynu.</span><span class="sxs-lookup"><span data-stu-id="604de-110">Specifies the name of the geographic location of the vault.</span></span>

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

### <span data-ttu-id="604de-111">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="604de-111">-Name</span></span>
<span data-ttu-id="604de-112">Określa nazwę magazynu, który ma zostać utworzony.</span><span class="sxs-lookup"><span data-stu-id="604de-112">Specifies the name of the vault to create.</span></span>

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

### <span data-ttu-id="604de-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="604de-113">-ResourceGroupName</span></span>
<span data-ttu-id="604de-114">Określa nazwę grupy zasobów platformy Azure, w której należy utworzyć lub z której ma zostać pobrany określony obiekt usług Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="604de-114">Specifies the name of the Azure resource group in which to create or from which to retrieve the specified Recovery Services object.</span></span>

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

### <span data-ttu-id="604de-115">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="604de-115">-Confirm</span></span>
<span data-ttu-id="604de-116">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="604de-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="604de-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="604de-117">-WhatIf</span></span>
<span data-ttu-id="604de-118">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="604de-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="604de-119">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="604de-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="604de-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="604de-120">-DefaultProfile</span></span>
<span data-ttu-id="604de-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="604de-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="604de-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="604de-122">CommonParameters</span></span>
<span data-ttu-id="604de-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="604de-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="604de-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="604de-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="604de-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="604de-125">INPUTS</span></span>

## <span data-ttu-id="604de-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="604de-126">OUTPUTS</span></span>

### <span data-ttu-id="604de-127">Microsoft. Azure. Commands. RecoveryServices. ARSVault</span><span class="sxs-lookup"><span data-stu-id="604de-127">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="604de-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="604de-128">NOTES</span></span>

## <span data-ttu-id="604de-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="604de-129">RELATED LINKS</span></span>

[<span data-ttu-id="604de-130">Get-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="604de-130">Get-AzureRmRecoveryServicesVault</span></span>](./Get-AzureRmRecoveryServicesVault.md)

[<span data-ttu-id="604de-131">Get-AzureRmRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="604de-131">Get-AzureRmRecoveryServicesVaultSettingsFile</span></span>](./Get-AzureRmRecoveryServicesVaultSettingsFile.md)

[<span data-ttu-id="604de-132">Remove-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="604de-132">Remove-AzureRmRecoveryServicesVault</span></span>](./Remove-AzureRmRecoveryServicesVault.md)


