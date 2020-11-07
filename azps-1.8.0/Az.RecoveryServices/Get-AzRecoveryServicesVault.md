---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 818B5302-91EE-425F-B1CD-86B626F1B7A3
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVault.md
ms.openlocfilehash: 5dfe76ad08c59a661d6907c65a53da9397f0a66d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93708647"
---
# <span data-ttu-id="73818-101">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="73818-101">Get-AzRecoveryServicesVault</span></span>

## <span data-ttu-id="73818-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="73818-102">SYNOPSIS</span></span>
<span data-ttu-id="73818-103">Pobiera listę magazynów usług odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="73818-103">Gets a list of Recovery Services vaults.</span></span>

## <span data-ttu-id="73818-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="73818-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesVault [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="73818-105">Opis</span><span class="sxs-lookup"><span data-stu-id="73818-105">DESCRIPTION</span></span>
<span data-ttu-id="73818-106">Polecenie cmdlet **Get-AzRecoveryServicesVault** pobiera listę magazynów usług odzyskiwania w bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="73818-106">The **Get-AzRecoveryServicesVault** cmdlet gets a list of Recovery Services vaults in the current subscription.</span></span>

## <span data-ttu-id="73818-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="73818-107">EXAMPLES</span></span>

### <span data-ttu-id="73818-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="73818-108">Example 1</span></span>
```
PS C:\> Get-AzRecoveryServicesVault
```

<span data-ttu-id="73818-109">Pobierz listę magazynów w wybranej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="73818-109">Get the list of vault in selected subscription.</span></span>

### <span data-ttu-id="73818-110">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="73818-110">Example 2</span></span>
```
PS C:\> Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup"
```

<span data-ttu-id="73818-111">Pobierz listę magazynów w grupie zasób w wybranej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="73818-111">Get the list of vault in resource group in selected subscription.</span></span>

### <span data-ttu-id="73818-112">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="73818-112">Example 3</span></span>
```
PS C:\> Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
```

<span data-ttu-id="73818-113">Pobierz magazyn w grupie zasobów o podanej nazwie.</span><span class="sxs-lookup"><span data-stu-id="73818-113">Get the vault in resource group with given name.</span></span>

## <span data-ttu-id="73818-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="73818-114">PARAMETERS</span></span>

### <span data-ttu-id="73818-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73818-115">-DefaultProfile</span></span>
<span data-ttu-id="73818-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="73818-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="73818-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="73818-117">-Name</span></span>
<span data-ttu-id="73818-118">Określa nazwę magazynu, którego ma dotyczyć kwerenda.</span><span class="sxs-lookup"><span data-stu-id="73818-118">Specifies the name of the vault to query for.</span></span>

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

### <span data-ttu-id="73818-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="73818-119">-ResourceGroupName</span></span>
<span data-ttu-id="73818-120">Określa nazwę grupy zasobów platformy Azure, w której należy utworzyć lub z której ma zostać pobrany określony obiekt usług Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="73818-120">Specifies the name of the Azure resource group in which to create or from which to retrieve the specified Recovery Services object.</span></span>

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

### <span data-ttu-id="73818-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73818-121">CommonParameters</span></span>
<span data-ttu-id="73818-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="73818-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73818-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="73818-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73818-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="73818-124">INPUTS</span></span>

### <span data-ttu-id="73818-125">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="73818-125">None</span></span>

## <span data-ttu-id="73818-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="73818-126">OUTPUTS</span></span>

### <span data-ttu-id="73818-127">Microsoft. Azure. Commands. RecoveryServices. ARSVault</span><span class="sxs-lookup"><span data-stu-id="73818-127">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="73818-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="73818-128">NOTES</span></span>

## <span data-ttu-id="73818-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="73818-129">RELATED LINKS</span></span>

[<span data-ttu-id="73818-130">Get-AzRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="73818-130">Get-AzRecoveryServicesVaultSettingsFile</span></span>](./Get-AzRecoveryServicesVaultSettingsFile.md)

[<span data-ttu-id="73818-131">Nowe — AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="73818-131">New-AzRecoveryServicesVault</span></span>](./New-AzRecoveryServicesVault.md)

[<span data-ttu-id="73818-132">Remove-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="73818-132">Remove-AzRecoveryServicesVault</span></span>](./Remove-AzRecoveryServicesVault.md)


