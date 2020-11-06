---
external help file: Microsoft.Azure.Commands.RecoveryServices.ARM.dll-Help.xml
Module Name: AzureRM.RecoveryServices
ms.assetid: 818B5302-91EE-425F-B1CD-86B626F1B7A3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Get-AzureRmRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Get-AzureRmRecoveryServicesVault.md
ms.openlocfilehash: bd9b47b54cb609a06da10488007f55d91d157b90
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93550811"
---
# <span data-ttu-id="4a392-101">Get-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="4a392-101">Get-AzureRmRecoveryServicesVault</span></span>

## <span data-ttu-id="4a392-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4a392-102">SYNOPSIS</span></span>
<span data-ttu-id="4a392-103">Pobiera listę magazynów usług odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="4a392-103">Gets a list of Recovery Services vaults.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4a392-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4a392-104">SYNTAX</span></span>

```
Get-AzureRmRecoveryServicesVault [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4a392-105">Opis</span><span class="sxs-lookup"><span data-stu-id="4a392-105">DESCRIPTION</span></span>
<span data-ttu-id="4a392-106">Polecenie cmdlet **Get-AzureRmRecoveryServicesVault** pobiera listę magazynów usług odzyskiwania w bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="4a392-106">The **Get-AzureRmRecoveryServicesVault** cmdlet gets a list of Recovery Services vaults in the current subscription.</span></span>

## <span data-ttu-id="4a392-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4a392-107">EXAMPLES</span></span>

## <span data-ttu-id="4a392-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4a392-108">PARAMETERS</span></span>

### <span data-ttu-id="4a392-109">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="4a392-109">-Name</span></span>
<span data-ttu-id="4a392-110">Określa nazwę magazynu, którego ma dotyczyć kwerenda.</span><span class="sxs-lookup"><span data-stu-id="4a392-110">Specifies the name of the vault to query for.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a392-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a392-111">-ResourceGroupName</span></span>
<span data-ttu-id="4a392-112">Określa nazwę grupy zasobów platformy Azure, w której należy utworzyć lub z której ma zostać pobrany określony obiekt usług Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="4a392-112">Specifies the name of the Azure resource group in which to create or from which to retrieve the specified Recovery Services object.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a392-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a392-113">-DefaultProfile</span></span>
<span data-ttu-id="4a392-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4a392-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4a392-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a392-115">CommonParameters</span></span>
<span data-ttu-id="4a392-116">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4a392-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a392-117">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4a392-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a392-118">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4a392-118">INPUTS</span></span>

## <span data-ttu-id="4a392-119">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4a392-119">OUTPUTS</span></span>

### <span data-ttu-id="4a392-120">System. Collections. Generic. list "1 [Microsoft. Azure. Commands. RecoveryServices. ARSVault]</span><span class="sxs-lookup"><span data-stu-id="4a392-120">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.RecoveryServices.ARSVault]</span></span>

## <span data-ttu-id="4a392-121">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4a392-121">NOTES</span></span>

## <span data-ttu-id="4a392-122">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4a392-122">RELATED LINKS</span></span>

[<span data-ttu-id="4a392-123">Get-AzureRmRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="4a392-123">Get-AzureRmRecoveryServicesVaultSettingsFile</span></span>](./Get-AzureRmRecoveryServicesVaultSettingsFile.md)

[<span data-ttu-id="4a392-124">Nowe — AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="4a392-124">New-AzureRmRecoveryServicesVault</span></span>](./New-AzureRmRecoveryServicesVault.md)

[<span data-ttu-id="4a392-125">Remove-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="4a392-125">Remove-AzureRmRecoveryServicesVault</span></span>](./Remove-AzureRmRecoveryServicesVault.md)


