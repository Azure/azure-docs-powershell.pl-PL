---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 5C788778-58A4-4798-AB66-1D3562BB9338
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/add-azurermdatalakestoretrustedidprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Add-AzureRmDataLakeStoreTrustedIdProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Add-AzureRmDataLakeStoreTrustedIdProvider.md
ms.openlocfilehash: a8c3e560ed66be9ae72d9f33e73af268e9fd5f85
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93548731"
---
# <span data-ttu-id="ddbf6-101">Add-AzureRmDataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="ddbf6-101">Add-AzureRmDataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="ddbf6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ddbf6-102">SYNOPSIS</span></span>
<span data-ttu-id="ddbf6-103">Dodaje zaufanego dostawcę tożsamości do określonego konta usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="ddbf6-103">Adds a trusted identity provider to the specified Data Lake Store account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ddbf6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ddbf6-104">SYNTAX</span></span>

```
Add-AzureRmDataLakeStoreTrustedIdProvider [-Account] <String> [-Name] <String> [-ProviderEndpoint] <String>
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ddbf6-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ddbf6-105">DESCRIPTION</span></span>
<span data-ttu-id="ddbf6-106">Polecenie cmdlet **Add-AzureRmDataLakeStoreTrustedIdProvider** umożliwia dodanie zaufanego dostawcy tożsamości do określonego konta usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="ddbf6-106">The **Add-AzureRmDataLakeStoreTrustedIdProvider** cmdlet adds a trusted identity provider to the specified Data Lake Store account.</span></span>

## <span data-ttu-id="ddbf6-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ddbf6-107">EXAMPLES</span></span>

### <span data-ttu-id="ddbf6-108">Przykład 1. Dodaj zaufanego dostawcę tożsamości</span><span class="sxs-lookup"><span data-stu-id="ddbf6-108">Example 1: Add a trusted identity provider</span></span>
```
PS C:\> Add-AzureRmDataLakeStoreTrustedIdProvider -AccountName "ContosoADL" -Name MyProvider -ProviderEndpoint "https://sts.windows.net/6b04908c-b91f-40ce-8024-7ee8a4fd6150"
```

<span data-ttu-id="ddbf6-109">Dodaje dostawcę "The dostarczającego" do konta "ContosoADL" z punktem końcowym dostawcy " https://sts.windows.net/6b04908c-b91f-40ce-8024-7ee8a4fd6150 "</span><span class="sxs-lookup"><span data-stu-id="ddbf6-109">Adds the provider "MyProvider" to account "ContosoADL" with the provider endpoint "https://sts.windows.net/6b04908c-b91f-40ce-8024-7ee8a4fd6150"</span></span>

## <span data-ttu-id="ddbf6-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ddbf6-110">PARAMETERS</span></span>

### <span data-ttu-id="ddbf6-111">— Konto</span><span class="sxs-lookup"><span data-stu-id="ddbf6-111">-Account</span></span>
<span data-ttu-id="ddbf6-112">Nazwa konta usługi Data Lake Store, do którego ma zostać dodany określony zaufany dostawca tożsamości.</span><span class="sxs-lookup"><span data-stu-id="ddbf6-112">The name of the Data Lake Store account to add the specified trusted identity provider to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ddbf6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ddbf6-113">-DefaultProfile</span></span>
<span data-ttu-id="ddbf6-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="ddbf6-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ddbf6-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ddbf6-115">-Name</span></span>
<span data-ttu-id="ddbf6-116">Nazwa zaufanego dostawcy tożsamości, który ma zostać dodany</span><span class="sxs-lookup"><span data-stu-id="ddbf6-116">The name of the trusted identity provider to add</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ddbf6-117">-ProviderEndpoint</span><span class="sxs-lookup"><span data-stu-id="ddbf6-117">-ProviderEndpoint</span></span>
<span data-ttu-id="ddbf6-118">Prawidłowy punkt końcowy zaufanego dostawcy w formacie: https://sts.windows.net/ \<provider identity\> "</span><span class="sxs-lookup"><span data-stu-id="ddbf6-118">The valid trusted provider endpoint in the format: https://sts.windows.net/\<provider identity\>"</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ddbf6-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ddbf6-119">-ResourceGroupName</span></span>
<span data-ttu-id="ddbf6-120">Nazwa grupy zasobów, pod którą konto ma dodać zaufanego dostawcę tożsamości.</span><span class="sxs-lookup"><span data-stu-id="ddbf6-120">Name of resource group under which the account to add the trusted identity provider is.</span></span>

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

### <span data-ttu-id="ddbf6-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ddbf6-121">-Confirm</span></span>
<span data-ttu-id="ddbf6-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ddbf6-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ddbf6-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ddbf6-123">-WhatIf</span></span>
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

### <span data-ttu-id="ddbf6-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ddbf6-124">CommonParameters</span></span>
<span data-ttu-id="ddbf6-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ddbf6-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ddbf6-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ddbf6-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ddbf6-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ddbf6-127">INPUTS</span></span>

### <span data-ttu-id="ddbf6-128">System. String</span><span class="sxs-lookup"><span data-stu-id="ddbf6-128">System.String</span></span>

## <span data-ttu-id="ddbf6-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ddbf6-129">OUTPUTS</span></span>

### <span data-ttu-id="ddbf6-130">Microsoft. Azure. Commands. DataLakeStore. models. DataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="ddbf6-130">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="ddbf6-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ddbf6-131">NOTES</span></span>

## <span data-ttu-id="ddbf6-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ddbf6-132">RELATED LINKS</span></span>
