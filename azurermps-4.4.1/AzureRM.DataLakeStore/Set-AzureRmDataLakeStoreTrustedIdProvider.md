---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: BDEF8BAA-0C64-465D-9ED4-6FEFC1E850CC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreTrustedIdProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreTrustedIdProvider.md
ms.openlocfilehash: 12e84ee5456acc0c56eed0f35b0bf3c23813b31f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527594"
---
# <span data-ttu-id="6b543-101">Set-AzureRmDataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="6b543-101">Set-AzureRmDataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="6b543-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6b543-102">SYNOPSIS</span></span>
<span data-ttu-id="6b543-103">Modyfikuje określonego zaufanego dostawcę tożsamości w określonej usłudze Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="6b543-103">Modifies the specified trusted identity provider in the specified Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6b543-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6b543-104">SYNTAX</span></span>

```
Set-AzureRmDataLakeStoreTrustedIdProvider [-Account] <String> [-Name] <String> [-ProviderEndpoint] <String>
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6b543-105">Opis</span><span class="sxs-lookup"><span data-stu-id="6b543-105">DESCRIPTION</span></span>
<span data-ttu-id="6b543-106">Polecenie cmdlet **Set-AzureRmDataLakeStoreTrustedIdProvider** modyfikuje określonego zaufanego dostawcę tożsamości w określonej usłudze Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="6b543-106">The **Set-AzureRmDataLakeStoreTrustedIdProvider** cmdlet modifies the specified trusted identity provider in the specified Data Lake Store.</span></span>

## <span data-ttu-id="6b543-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6b543-107">EXAMPLES</span></span>

### <span data-ttu-id="6b543-108">Przykład 1: aktualizowanie punktu końcowego zaufanego dostawcy tożsamości</span><span class="sxs-lookup"><span data-stu-id="6b543-108">Example 1: Update a Trusted Identity Provider Endpoint</span></span>
```
PS C:\> Set-AzureRmDataLakeStoreTrustedIdProvider -AccountName "ContosoADL" -Name MyProvider -ProviderEndpoint "https://sts.windows.net/6b04908c-b91f-40ce-8024-7ee8a4fd6150"
```

<span data-ttu-id="6b543-109">Spowoduje to zaktualizowanie dostawcy endpoing dla reguły zapory "Moja dostarczająca" na koncie "ContosoADL" na " https://sts.windows.net/6b04908c-b91f-40ce-8024-7ee8a4fd6150 "</span><span class="sxs-lookup"><span data-stu-id="6b543-109">This updates the provider endpoing for firewall rule "MyProvider" in account "ContosoADL" to "https://sts.windows.net/6b04908c-b91f-40ce-8024-7ee8a4fd6150"</span></span>

## <span data-ttu-id="6b543-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6b543-110">PARAMETERS</span></span>

### <span data-ttu-id="6b543-111">— Konto</span><span class="sxs-lookup"><span data-stu-id="6b543-111">-Account</span></span>
<span data-ttu-id="6b543-112">Konto usługi Data Lake Store umożliwiające dodanie dostawcy zaufanej tożsamości do</span><span class="sxs-lookup"><span data-stu-id="6b543-112">The Data Lake Store account to add the trusted identity provider to</span></span>

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

### <span data-ttu-id="6b543-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="6b543-113">-Name</span></span>
<span data-ttu-id="6b543-114">Nazwa zaufanego dostawcy tożsamości.</span><span class="sxs-lookup"><span data-stu-id="6b543-114">The name of the trusted identity provider.</span></span>

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

### <span data-ttu-id="6b543-115">-ProviderEndpoint</span><span class="sxs-lookup"><span data-stu-id="6b543-115">-ProviderEndpoint</span></span>
<span data-ttu-id="6b543-116">Prawidłowy punkt końcowy zaufanego dostawcy w formacie: https://sts.windows.net/\<provider identity\></span><span class="sxs-lookup"><span data-stu-id="6b543-116">The valid trusted provider endpoint in the format: https://sts.windows.net/\<provider identity\></span></span>

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

### <span data-ttu-id="6b543-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b543-117">-ResourceGroupName</span></span>
<span data-ttu-id="6b543-118">Określa nazwę grupy zasobów zawierającej konto, dla którego ma zostać zaktualizowany zaufany dostawca tożsamości.</span><span class="sxs-lookup"><span data-stu-id="6b543-118">Specifies the name of the resource group that contains the account to update the trusted identity provider for.</span></span>

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

### <span data-ttu-id="6b543-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6b543-119">-Confirm</span></span>
<span data-ttu-id="6b543-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6b543-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6b543-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6b543-121">-WhatIf</span></span>
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

### <span data-ttu-id="6b543-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b543-122">-DefaultProfile</span></span>
<span data-ttu-id="6b543-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6b543-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6b543-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b543-124">CommonParameters</span></span>
<span data-ttu-id="6b543-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b543-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b543-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6b543-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b543-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6b543-127">INPUTS</span></span>

## <span data-ttu-id="6b543-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6b543-128">OUTPUTS</span></span>

### <span data-ttu-id="6b543-129">DataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="6b543-129">DataLakeStoreTrustedIdProvider</span></span>
<span data-ttu-id="6b543-130">Zaktualizowany zaufany dostawca tożsamości.</span><span class="sxs-lookup"><span data-stu-id="6b543-130">The updated trusted identity provider.</span></span>

## <span data-ttu-id="6b543-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6b543-131">NOTES</span></span>

## <span data-ttu-id="6b543-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6b543-132">RELATED LINKS</span></span>

