---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 0EB5C25C-D0A1-4444-AEA2-C963D5069CFC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreAccount.md
ms.openlocfilehash: f9ebe1a541baf46e831dbe95b54b2881a03e7454
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717852"
---
# <span data-ttu-id="f8690-101">Set-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="f8690-101">Set-AzureRmDataLakeStoreAccount</span></span>

## <span data-ttu-id="f8690-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f8690-102">SYNOPSIS</span></span>
<span data-ttu-id="f8690-103">Modyfikuje konto w usłudze Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="f8690-103">Modifies a Data Lake Store account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f8690-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f8690-104">SYNTAX</span></span>

```
Set-AzureRmDataLakeStoreAccount [-Name] <String> [[-DefaultGroup] <String>] [[-Tags] <Hashtable>]
 [[-TrustedIdProviderState] <TrustedIdProviderState>] [[-FirewallState] <FirewallState>]
 [[-ResourceGroupName] <String>] [-Tier <TierType>] [-AllowAzureIpState <FirewallAllowAzureIpsState>]
 [-KeyVersion <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f8690-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f8690-105">DESCRIPTION</span></span>
<span data-ttu-id="f8690-106">Polecenie cmdlet **Set-AzureRmDataLakeStoreAccount** modyfikuje konto usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="f8690-106">The **Set-AzureRmDataLakeStoreAccount** cmdlet modifies a Data Lake Store account.</span></span>

## <span data-ttu-id="f8690-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f8690-107">EXAMPLES</span></span>

### <span data-ttu-id="f8690-108">Przykład 1. Dodawanie znacznika do konta</span><span class="sxs-lookup"><span data-stu-id="f8690-108">Example 1: Add a tag to an account</span></span>
```
PS C:\>Set-AzureRmDataLakeStoreAccount -Name "ContosoADL" -Tags @{"stage"="production"}
```

<span data-ttu-id="f8690-109">To polecenie umożliwia dodanie określonego tagu do konta usługi Data Lake Store o nazwie ContosoADL.</span><span class="sxs-lookup"><span data-stu-id="f8690-109">This command adds the specified tag to the Data Lake Store account named ContosoADL.</span></span>

## <span data-ttu-id="f8690-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f8690-110">PARAMETERS</span></span>

### <span data-ttu-id="f8690-111">-AllowAzureIpState</span><span class="sxs-lookup"><span data-stu-id="f8690-111">-AllowAzureIpState</span></span>
<span data-ttu-id="f8690-112">Opcjonalnie Zezwalaj na używanie/blokowanie początkowych adresów IP platformy Azure za pośrednictwem zapory.</span><span class="sxs-lookup"><span data-stu-id="f8690-112">Optionally allow/block Azure originating IPs through the firewall.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.DataLake.Store.Models.FirewallAllowAzureIpsState]
Parameter Sets: (All)
Aliases: 
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8690-113">-Domyślna</span><span class="sxs-lookup"><span data-stu-id="f8690-113">-DefaultGroup</span></span>
<span data-ttu-id="f8690-114">Określa identyfikator grupy katalogów usługi AzureActive.</span><span class="sxs-lookup"><span data-stu-id="f8690-114">Specifies the ID of an AzureActive Directory group.</span></span>
<span data-ttu-id="f8690-115">Ta grupa jest domyślną grupą tworzonych plików i folderów.</span><span class="sxs-lookup"><span data-stu-id="f8690-115">This group is the default group for files and folders that you create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8690-116">-FirewallState</span><span class="sxs-lookup"><span data-stu-id="f8690-116">-FirewallState</span></span>
<span data-ttu-id="f8690-117">Opcjonalnie Włącz lub Wyłącz istniejące reguły zapory.</span><span class="sxs-lookup"><span data-stu-id="f8690-117">Optionally enable or disable existing firewall rules.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.DataLake.Store.Models.FirewallState]
Parameter Sets: (All)
Aliases: 
Accepted values: Enabled, Disabled

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8690-118">-Wersja-</span><span class="sxs-lookup"><span data-stu-id="f8690-118">-KeyVersion</span></span>
<span data-ttu-id="f8690-119">Jeśli typ szyfrowania jest przypisany przez użytkownika, użytkownik może obrócić swoją wersję klucza za pomocą tego parametru.</span><span class="sxs-lookup"><span data-stu-id="f8690-119">If the encryption type is User assigned, the user can rotate their key version with this parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8690-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f8690-120">-Name</span></span>
<span data-ttu-id="f8690-121">Określa nazwę konta usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="f8690-121">Specifies the name of a Data Lake Store account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8690-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8690-122">-ResourceGroupName</span></span>
<span data-ttu-id="f8690-123">Określa nazwę grupy zasobów zawierającej konto usługi Data Lake Store do zmodyfikowania.</span><span class="sxs-lookup"><span data-stu-id="f8690-123">Specifies the name of the resource group that contains the Data Lake Store account to modify.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8690-124">-Tagi</span><span class="sxs-lookup"><span data-stu-id="f8690-124">-Tags</span></span>
<span data-ttu-id="f8690-125">Określa znaczniki jako pary klucz-wartość.</span><span class="sxs-lookup"><span data-stu-id="f8690-125">Specifies tags as key-value pairs.</span></span>
<span data-ttu-id="f8690-126">Za pomocą znaczników możesz identyfikować konta usługi Data Lake Store z innych zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="f8690-126">You can use tags to identify a Data Lake Store account from other Azure resources.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8690-127">-Warstwowy</span><span class="sxs-lookup"><span data-stu-id="f8690-127">-Tier</span></span>
<span data-ttu-id="f8690-128">Pożądana warstwa zobowiązań do użycia dla tego konta.</span><span class="sxs-lookup"><span data-stu-id="f8690-128">The desired commitment tier for this account to use.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.DataLake.Store.Models.TierType]
Parameter Sets: (All)
Aliases: 
Accepted values: Consumption, Commitment1TB, Commitment10TB, Commitment100TB, Commitment500TB, Commitment1PB, Commitment5PB

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8690-129">-TrustedIdProviderState</span><span class="sxs-lookup"><span data-stu-id="f8690-129">-TrustedIdProviderState</span></span>
<span data-ttu-id="f8690-130">Opcjonalnie Włącz lub Wyłącz istniejących dostawców zaufanych identyfikatorów.</span><span class="sxs-lookup"><span data-stu-id="f8690-130">Optionally enable or disable the existing trusted ID providers.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.DataLake.Store.Models.TrustedIdProviderState]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8690-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8690-131">-DefaultProfile</span></span>
<span data-ttu-id="f8690-132">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f8690-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f8690-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8690-133">CommonParameters</span></span>
<span data-ttu-id="f8690-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8690-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8690-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f8690-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8690-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f8690-136">INPUTS</span></span>

## <span data-ttu-id="f8690-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f8690-137">OUTPUTS</span></span>

### <span data-ttu-id="f8690-138">PSDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="f8690-138">PSDataLakeStoreAccount</span></span>
<span data-ttu-id="f8690-139">Zaktualizowane dane konta.</span><span class="sxs-lookup"><span data-stu-id="f8690-139">The updated account details.</span></span>

## <span data-ttu-id="f8690-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f8690-140">NOTES</span></span>

## <span data-ttu-id="f8690-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f8690-141">RELATED LINKS</span></span>

[<span data-ttu-id="f8690-142">Get-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="f8690-142">Get-AzureRmDataLakeStoreAccount</span></span>](./Get-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="f8690-143">Nowe — AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="f8690-143">New-AzureRmDataLakeStoreAccount</span></span>](./New-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="f8690-144">Remove-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="f8690-144">Remove-AzureRmDataLakeStoreAccount</span></span>](./Remove-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="f8690-145">Test — AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="f8690-145">Test-AzureRmDataLakeStoreAccount</span></span>](./Test-AzureRmDataLakeStoreAccount.md)


